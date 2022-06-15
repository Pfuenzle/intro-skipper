# Changelog

## v0.1.6.0 (unreleased)
* Write EDL files with intro timestamps

## v0.1.5.0 (unreleased)
* Use `ffmpeg` to generate audio fingerprints instead of `fpcalc`
  * Requires that the installed version of `ffmpeg`:
    * Was compiled with the `--enable-chromaprint` option
    * Understands the `-fp_format raw` flag
  * `jellyfin-ffmpeg 5.0.1-5` meets both of these requirements
* Version API endpoints
  * See [api.md](docs/api.md) for detailed documentation on how clients can work with this plugin
* Add commit hash to unstable builds
* Log media paths that are unable to be fingerprinted
* Report failure to the UI if the episode analysis queue is empty
* Allow customizing degrees of parallelism
  * Warning: Using a value that is too high will result in system instability

## v0.1.0.0 (2022-06-09)
* Add option to automatically skip intros
* Cache audio fingerprints by default
* Add fingerprint visualizer
* Add button to erase all previously discovered intro timestamps
* Made saving settings more reliable
* Switch to new fingerprint comparison algorithm
  * If you would like to test the new comparison algorithm, you will have to erase all previously discovered introduction timestamps.

## v0.0.0.3 (2022-06-21)
* Fix `fpcalc` version check

## v0.0.0.2 (2022-06-21)
* Analyze multiple seasons in parallel
* Reanalyze episodes with an unusually short or long intro sequence
* Check installed `fpcalc` version
* Clarify installation instructions

## v0.0.0.1 (2022-06-10)
* First alpha build
