<div align="center">
  <a href="https://elementary.io" align="center">
    <center align="center">
      <img src="https://raw.githubusercontent.com/elementary/brand/master/logomark-black.png" alt="elementary" align="center">
    </center>
  </a>
  <br>
  <h1 align="center"><center>elementary OS</center></h1>
  <h3 align="center"><center>Build scripts for image creation</center></h3>
  <br>
  <br>
</div>

<p align="center">
  <img src="https://github.com/elementary/os/workflows/stable/badge.svg" alt="Stable">
  <img src="https://github.com/elementary/os/workflows/daily/badge.svg" alt="Daily">
</p>

---

## Building Locally

As elementary OS is built with the Debian version of `live-build`, not the Ubuntu patched version, it's easiest to build an elementary .iso in a Debian VM or container. This prevents messing up your host system too.

The following example uses Docker and assumes you have Docker correctly installed and set up:

 1) Clone this project & `cd` into it:

    ```
    git clone https://github.com/Shomeis-Eskandari/elementary && cd elementary
    ```

 2) Configure the channel in the `etc/terraform.conf` (stable, daily).

 3) Run the build:

    ```
    docker-compose up
    ```

 4) When done, your image will be in the `artifacts` folder.

## ReBuild 

  ```
  docker container rm -f elementary_os
  docker image rm -f elementary_os
  rm -Rf ./artifacts/*
  rm -Rf ./tmp/*
  ```

## Further Information

More information about the concepts behind `live-build` and the technical decisions made to arrive at this set of tools to build an .iso can be found [on the wiki](https://github.com/elementary/os/wiki/Building-iso-Images).
