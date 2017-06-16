# Hapa'o Test Coverage Tool

Test coverage is about assessing the relevance of unit tests against the tested application. It is widely acknowledged that software with “good” test coverage is more robust against unanticipated execution, thus lowering the maintenance cost. However, insuring good quality coverage is challenging, especially since most of the available test coverage tools do not discriminate between software components that require a "strong" coverage from the components that require less attention from the unit tests.

The word Hapa'o (also written Hapao) belongs to the Rapanui language, still spoken in Easter Island.

Hapa'o: to take care, keep (someone or something) safe and provided for

Have fun! The Hapao Team

### Getting Started

Hapao is an innovative test coverage tool, implemented in the VisualWorks and Pharo Smalltalk programming languages. It employs an effective and intuitive graphical representation to visually assess the quality of the coverage. A combination of appropriate metrics and relations visually shapes methods and classes, which indicates to the programmer whether more effort on testing is required.

### Prerequisites

Hapa'o is available under the MIT License, for the VisualWorks and Pharo platforms.

Use [Pharo](http://pharo.org/download) or [VisualWorks](http://www.cincomsmalltalk.com/main/products/)

### Installing

Hapa'o is available on the public Cincom repository under the Spy project repository.

![VisualWorks](https://dl.dropboxusercontent.com/s/mwpxkaitlcfvsrn/spy.png?dl=0)

To download Hapa'o in a fresh Pharo image. Execute the following in a workspace:

```
Gofer new
	squeaksource: 'Spy';
	package: 'ConfigurationOfSpy';
	load.
(Smalltalk at: #ConfigurationOfSpy) perform: #loadDefault
```

## Built With

* [Roassal](http://agilevisualization.com/)
* [Pharo](http://pharo.org/)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone who's code was used
* Inspiration
* etc
