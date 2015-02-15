# Gulp JSHint checkstyle reporter

Writes checkstyle output to a stream. This can be used to report JSHint results to **Jenkins**.

## Installation
```bash
npm install --save-dev gulp-jshint-checkstyle-reporter
```

## Usage

### Gulp

```javascript
var gulp = require('gulp');
var jshint = require('gulp-jshint');
var checkstyleReporter = require('gulp-jshint-checkstyle-reporter');

gulp.task('jshint', function() {
	gulp.src('*.js')
		.pipe(jshint())
		.pipe(checkstyleReporter())
		.pipe(gulp.dest('target/checkstyle-reports'));
});
```

#### Options

You could optionally pass an options object into the `checkstyleReporter`
function:

- *filename* (defaults to *checkstyle.xml*). Default filename of the output xml
  file.
- Any other jshint-checkstyle reporter option.
