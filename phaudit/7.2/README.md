# Phaudit

- [`7.2`, `latest` (*phaudit/7.2/Dockerfile*)](https://github.com/mykiwi/dockerfiles/tree/master/phaudit/7.2/Dockerfile)
- [`7.1` (*phaudit/7.1/Dockerfile*)](https://github.com/mykiwi/dockerfiles/tree/master/phaudit/7.1/Dockerfile)
- [`7.0` (*phaudit/7.0/Dockerfile*)](https://github.com/mykiwi/dockerfiles/tree/master/phaudit/7.0/Dockerfile)

A simple docker images to run some phpqatools on your php project

## Available tools

* [PHPLoc](http://github.com/sebastianbergmann/phploc) as `phploc`
* [PHP_Depend](http://pdepend.org/) as `pdepend`
* [PHP Mess Detector](http://phpmd.org/) as `phpmd`
* [PHP_CodeSniffer](http://pear.php.net/PHP_CodeSniffer) as `phpcs` and `phpcbf`
* [PHP Copy/Paste Detector](http://github.com/sebastianbergmann/phpcpd) as `phpcpd`
* [PHP Dead Code Detector](http://github.com/sebastianbergmann/phpdcd) as `phpdcd`
* [PhpMetrics](http://www.phpmetrics.org/) as `phpmetrics`
* [PHP Coding Standards Fixer](http://cs.sensiolabs.org/) as `php-cs-fixer`
* [PHP Static Analysis Tool](https://github.com/phpstan/phpstan) as `phpstan`
* [Twig Coding Standards](https://github.com/allocine/twigcs) as `twigcs`

## Usage

Grab the image, and run one of tool with your project mounted in the work directory `/project` on this image:

```
cd my_php_project
docker pull mykiwi/phaudit
docker run -t -i -v `pwd`:/project mykiwi/phaudit phploc src/
```

---

Adapted from [jolicode/phaudit](https://hub.docker.com/r/jolicode/phaudit/)
