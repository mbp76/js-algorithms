# js-algorithms

A set of common algorithms implemented in JS. Includes binary search, selection
and insertion sort, merge sort, quicksort and breadth-first search.

## Installation

Start by downloading and building the project when necessary. The following
commands will do the job on most Debian based Linux distributions.

```bash
git clone https://github.com/marcbperez/js-algorithms
cd js-algorithms
```

## Usage

The examples can be used from the command-line with Node.js.

```bash
node src/binary-search.js
```

They can also be embedded in other modules.

```javascript
var algorithms = require('js-algorithms/src/binary-search.js');
console.log(algorithms.binarySearch(primes, 53));
```

Or included in an HTML document.

```html
<script src="js-algorithms/src/binary-search.js"></script>
<script>
  console.log(binarySearch(primes, 53));
</script>
```

## Testing

Test checks are executed automatically every time the project is built. Builds
can be done remotely or continuously on a development context. For continuous
integration and development use docker-compose. This is recommended to keep the
system clean while the project is built every time the sources change.

```bash
sudo docker-compose up
```

For continuous integration and development without any dependencies use the
Gradle wrapper. This is the best option if the wrapper is available and the
Docker context is not valid. For a full list of tasks, see
`sudo ./gradlew tasks --all`. For a CI cycle use `sudo ./gradlew --continuous`.

For continuous integration and development without Docker or the project wrapper
use Gradle directly. This will create the wrapper in case it is not present.
Similar to the above, for a CI cycle use `sudo gradle --continuous`. Gradle
3.4.1 is required for this to work. Plain Docker is also available for remote
integration tasks and alike. Build the image with `sudo docker build .` and run
a new container with it. Information on how to install Docker and docker-compose
can be found in their [official page][install-docker-compose]. A similar
installation guide is available [for Gradle][install-gradle].

## Troubleshooting

The [issue tracker][issue-tracker] intends to manage and compile bugs,
enhancements, proposals and tasks. Reading through its material or reporting to
its contributors via the platform is strongly recommended.

## Contributing

This project adheres to [Semantic Versioning][semver] and to certain syntax
conventions defined in [.editorconfig][editorconfig]. To get a list of changes
refer to the [CHANGELOG][changelog]. Only branches prefixed by *feature-*,
*hotfix-*, or *release-* will be considered:

  - Fork the project.
  - Create your new branch: `git checkout -b feature-my-feature develop`
  - Commit your changes: `git commit -am 'Added my new feature.'`
  - Push the branch: `git push origin feature-my-feature`
  - Submit a pull request.

## Credits

This project is created by [marcbperez][author] and maintained by its
[author][author] and contributors.

## License

This project is licensed under the [Apache License Version 2.0][license].

[author]: https://marcbperez.github.io
[issue-tracker]: https://github.com/marcbperez/js-algorithms/issues
[editorconfig]: .editorconfig
[changelog]: CHANGELOG.md
[license]: LICENSE
[semver]: http://semver.org
[install-docker-compose]: https://docs.docker.com/compose/install/
[install-gradle]: https://gradle.org/install
