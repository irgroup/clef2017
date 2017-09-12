# Material for CLEF2017 Poster presentation / short paper

This repository contains accompanying material to our short paper submitted and accepted at the [CLEF2017](http://clef2017.clef-initiative.eu/index.php) conference.

You can find the paper in the official [CLEF2017 conference proceedings](https://link.springer.com/book/10.1007/978-3-319-65813-1), or at the [arXiv](https://arxiv.org/abs/1706.06836).

## Getting Started

To get a copy of the materials, use either `git clone`, or download the repository's content as a compressed file (.zip) and extract it anywhere on your local file system.

### Prerequisites

Currently, OXPath is only supported on 64bit Linux-based operating systems. Java has to be installed on this system (version 8 or above). Optionally, the xvfb package has to be installed if you want to use the option to run Firefox in the X virtual framebuffer for the evaluation of OXPath expressions.

### Installation of XVFB (e.g. on Ubuntu 16.04)

```sh
$ sudo apt install xvfb
```

### Get OXPath

OXPath can be obtained from: [www.oxpath.org/download](http://www.oxpath.org/download) 

Pick the latest version of the CLI jar and save it to a convenient location.

## Running the example

### With OXPath 2.0

To run the example, fire up a command line where you extracted/cloned this repository to, and input the following command, where

-   `-query script/sowiport_solis_en.oxp`: reads the OXPath expression in the file `sowiport_solis_en.oxp` in the `script` subfolder
-   `-logfile VerboseLog4j.properties`: uses the provided custom logging configuration file for more verbose logging (recommended for OXPath beginners)
-   `-browser firefox_xvfb`: runs the OXPath evaluation with a virtual frame buffer
-   `-output output/sowiport_solis_en.xml`: re-directs the XML output to the file `sowiport_solis_en.xml` in the subfolder `output`
-   `-xml`: sets the output format to XML

```sh
$ java -jar oxpath-2.0-cli.jar -query script/sowiport_solis_de.oxp -logfile VerboseLog4j.properties -browser firefox_xvfb -output output/sowiport_solis_de.xml -xml
```

*Hint:* If your system is localized to German language, use `sowiport_solis_de` version of the script. Else, use the `sowiport_solis_en` version.


### With OXPath 2.0.2

(will be released soon, more info to follow)
<!--- Note to self: adjust when new version is officially released --->
<!--
To run the example, fire up a command line and input the following command, where

-   `-q sowiport_solis_de.oxp`: reads the OXPath expression in the file `sowiport_solis_de.oxp`
-   `-log VerboseLog4j.properties`: uses the provided custom logging configuration file for more verbose logging (recommended for OXPath beginners)
-   `-xvfb`: (optional) runs the OXPath evaluation with a virtual frame buffer
-   `-o sowiport_solis_de.xml`: re-directs the XML output to the file `sowiport_solis_de.xml`

```sh
$ java -jar oxpath-2.0-cli.jar -q bicc_WP.oxp -log VerboseLog4j.properties -xvfb -o bicc_WP.xml
```
-->

## Author

*   **Mandy Neumann** - *Second author of the article*

## License

This project is licensed under the Apache 2.0 License - see the [LICENSE](LICENSE) file for details.

<!--The OXPath executable contained in this repository is licensed under Apache 2.0 License.-->

## Acknowledgments

*   **Philipp Schaer** - *First author*