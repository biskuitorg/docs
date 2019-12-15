# Install Biskuit from source

<p class="uk-article-lead">When building Biskuit extensions, you can totally rely on a Biskuit installation from one of the release packages available at [biskuit.org](https://www.biskuit.org/download) or [from Github](https://github.com/biskuit/biskuit/releases).</p>

However, if you always want stay up to date with the current development version, you can install Biskuit from the source available on Github. This article explains, which steps you need to take.

<ul class="uk-list">
    <li><a href="#check-out-and-install">Check out and install</a></li>
    <li><a href="#stay-up-to-date">Stay up to date</a></li>
</ul>

## Check out and install

Make sure that [Composer](https://getcomposer.org/doc/00-intro.md#installation-nix) and [npm](https://www.npmjs.com/) are installed.

Clone the repository.

```
git clone --branch develop https://github.com/biskuit/biskuit.git
```

Navigate to the cloned directory and install PHP dependencies.

```
composer install
```

Install Node dependencies and build the front-end components:

```
npm install
```

To watch for local LESS asset changes, run `gulp watch`.

To watch for JS module changes, run `webpack --watch`.

When the installer has finished, point your browser to the Biskuit URL on your web server and follow the installer.

When you have a running Biskuit installation, use the Biskuit CLI to fetch translations. Without that, the interface will appear in English only.

```
php biskuit translation:fetch
```

## Stay up to date

If you've set up Biskuit from source, run these commands to get new commits and to rebuild everything you need.

```
git pull
composer install
npm install
```