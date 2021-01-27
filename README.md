# sanitize-filename

[![Clojars Project](https://img.shields.io/clojars/v/sanitize-filename.svg)](https://clojars.org/sanitize-filename)

Filename sanitization for Clojure and ClojureScript.
This is useful when you generate filenames for downloads from user input

Port of ruby's zaru library:

https://github.com/madrobby/zaru

## Installation
Add the following to your project.clj :dependencies:
### Leiningen
    [sanitize-filename "0.1.0"]

### Clojure CLI
    sanitize-filename/sanitize-filename {:mvn/version "0.1.0"}

### Clojure CLI / Repo
    fnumatic/sanitize-filename {:git/url "https://github.com/fnumatic/sanitize-filename.git"
                                :sha     "42dc97cbcca1e24bc4ebe6f2d9d789d64bb93365"}    
## Usage

    (require '[sanitize-filename.core :as sf])

    (sf/sanitize "/a/b/  我是c.zip")
    ; should return "$a$b$我是c.zip"

For more details, please refer zaru:
     https://github.com/madrobby/zaru

## Differences with zaru

1. no padding support
2. replace "/" with "$" instead of ""

## Other implementations

* [zaru](https://github.com/madrobby/zaru) (Ruby)
* [sanitize](https://github.com/ksze/sanitize) (Python)
* [owasp-java-fileio](https://github.com/augustd/owasp-java-fileio) (Java)
* [node-sanitize-filename](https://github.com/parshap/node-sanitize-filename) (JavaScript)

## License

Copyright © 2014 contributors

Released under the MIT license.
