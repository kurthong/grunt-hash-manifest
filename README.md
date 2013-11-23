# grunt-hash-manifest-fix-md5

*This plugin is just forked from grunt-hash-manifest[https://github.com/gseguin/grunt-hash-manifest] to have correct MD5 value. Original grunt-hash-manifest has two issues with MD5 generation like shown below.
- MD5 value is different from others[https://github.com/gseguin/grunt-hash-manifest/issues/1]
- Fixed to work with binary files[https://github.com/gseguin/grunt-hash-manifest/pull/2]

Creates manifest of files and associated hashes

## Getting Started
This plugin requires Grunt `~0.4.0`

```shell
npm install grunt-hash-manifest-fix-md5 --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-hash-manifest-fix-md5');
```

*This plugin was designed to work with Grunt 0.4.x.


### Options
- `algo` specifies which hashing algorithm to use. The default is `md5`. The choices are limited to what node's `crypto` module supports.
- `cwd` is the directory in which to expand the globbing patterns as well as the root for `dest`

### Usage Examples

```js
"hash-manifest": {
  dist: {
    options: {
        algo: "md5",
        cwd: "dist"
    },
    src: [ "**/*" ],
    dest: "MANIFEST"
  }
}
```
