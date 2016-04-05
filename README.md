Role Name
=========

Install [VIPS image processing software](http://www.vips.ecs.soton.ac.uk/) with bug-free OpenSlide support.

On Ubuntu 14.04, VIPS contains a bug where OpenSlide does not open some images properly.
This role installs VIPS's OpenSlide dependencies to reliably work around that bug.

Requirements
------------

This is intended to be run on a clean Ubuntu 14.04 system.

Role Variables
--------------

You may want to override the variables:
* `vips_openjpeg_path`: Path to fetch and build OpenJPEG.
* `vips_libtiff_path`: Path to fetch and build LibTIFF.
* `vips_openslide_path`: Path to fetch and build OpenSlide.

You can (but probably won't need to) override the variables:
* `vips_openjpeg_version`: Git commit-ish for fetching OpenJPEG.
* `vips_libtiff_version`: Git commit-ish for fetching LibTIFF.
* `vips_openslide_version`: Git commit-ish for fetching OpenSlide.
* `build_parallelism: "{{ ansible_processor_vcpus + 1 }}"

License
-------

Apache 2.0
