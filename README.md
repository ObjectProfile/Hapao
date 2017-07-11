# Hapa'o Test Coverage Tool

Test coverage is about assessing the relevance of unit tests against the tested application. It is widely acknowledged that software with “good” test coverage is more robust against unanticipated execution, thus lowering the maintenance cost. However, insuring good quality coverage is challenging, especially since most of the available test coverage tools do not discriminate between software components that require a "strong" coverage from the components that require less attention from the unit tests.

The word Hapa'o (also written Hapao) belongs to the Rapanui language, still spoken in Easter Island.

Hapa'o: to take care, keep (someone or something) safe and provided for

Have fun! The Hapao Team

### Getting Started

Hapao is an innovative test coverage tool, implemented in the VisualWorks and Pharo Smalltalk programming languages. It employs an effective and intuitive graphical representation to visually assess the quality of the coverage. A combination of appropriate metrics and relations visually shapes methods and classes, which indicates to the programmer whether more effort on testing is required.

### Prerequisites

Use [Pharo](http://pharo.org/download) or [VisualWorks](http://www.cincomsmalltalk.com/main/products/)

### Installing

Hapa'o is available on the public Cincom repository under the Spy project repository.

![VisualWorks](https://dl.dropboxusercontent.com/s/mwpxkaitlcfvsrn/spy.png?dl=0)

To download Hapa'o in a fresh Pharo image. Just open **World menu>Tools>Catalog Browser**, and install Spy2
![Spy2Pharo](https://dl.dropboxusercontent.com/s/w1jwxtvwos8y22n/spy2pharo.png?dl=0)

### How to use

In pharo Hapao is accesible from the **WorldMenu>>Hapao.**

<img src="https://dl.dropboxusercontent.com/s/onl2wlinmprg33e/hapomenu.png?dl=0" width="300">

For example select **Hapao @ Package...**

<img src="https://dl.dropboxusercontent.com/s/adwxhuhwv8ef77z/hapaoinputdialog.png?dl=0" width="400">
This box accepts regular expresions, this example uses: Trachel&#42;. Then a new inspector of hapao should appear,

<img src="https://dl.dropboxusercontent.com/s/o55l33f6585omj6/hapaoinspector.png?dl=0">

### Test blue print

<img src="https://dl.dropboxusercontent.com/s/evfi3tfchr0rq9g/hapao%20blueprint.png?dl=0">

The encapsulating boxes represent classes (Clazz, SubClazz and ClazzTest). Inheritance is indicated with an edge between classes. Subclasses are below their superclass. Clazz is the superclass of SubClazz. The superclass of ClazzTest is not part of the analysis. The green border within a class box indicates a unit test.

Inner boxes represent methods. Clazz defines five methods, a, b, c, d and e. SubClazz defines one method, f. Each method is represented as a small box, visually defined with fives dimensions:

* Height is the cyclomatic complexity of the method. Th more the method takes different paths at execution time, the taller the box will be (e.g. Method b).
* Width|is the number of different methods that call the method when running the tests. A wide method (f) means the method has been executed many times by the tests. A thin method (a, b, c) means the method has been executed zero to very a few times.
* gray intensity reflects the number of times the method has been executed. A dark method (d, f) has been executed many times. A light or gray-toned method (c) has been executed only a few times. 
* A red border color (light gray on a B&W printout) means the method has not been executed (a, b). A blue border indicates abstract methods while a green one indicates that the method is a test method, defined in a unit test.
* the call-flow on self variable is indicated with edges of connecting points. This happens if the body of a contains the expression self d, meaning that the message d is sent to self. The method a calls d on self. The method b calls d and c on self. Note that we are focusing on the call-flow instead of the control-flow.

### Contextual information

Passing the mouse over a method displays a contextual popup window and the class border color is turns red. This popup window gives the full name of the method <Clazz>>c:>, in addition to the invoking methods and invoked methods.

The popup window focused on the method from which it had been produced. The method is located at the center of the popup window. The incoming methods are situated in the upper section, while the outgoing methods are situated in the lower section.

The contextual popup window displays essential information about the context in which the method is used. For example, the method boundsOf: is invoked by three test methods and invokes many other non-complex methods (which could include utility methods). The window is displayed after a short delay in order to avoid image flickering when placing the mouse over two or more methods.

### Navigation

The following navigation options are accessible via contextual menus offered when right-clicking on an element in Hapa'o or in the system browser

* Inspect: Shows more details of one class, in the inspector
* Browse, Browse test: Shows this class with system browser.


From Hapao's top menu you have the following options:

* ?: will show the basic legend of Hapao

<img src="https://dl.dropboxusercontent.com/s/cb3afblrehop9w9/hapao%20legend.png?dl=0">

* Find: will open spotter and find elements in hapao

<img src="https://dl.dropboxusercontent.com/s/l7ib2whpbl7aoe3/hapao%20spotter.png?dl=0" width="400">
* get list: return the list of the elements
<img src="https://dl.dropboxusercontent.com/s/1nx2ahcmfghpxj5/hapao%20list.png?dl=0" width="400">
* matrix: shows a simple matrix of the methods
<img src="https://dl.dropboxusercontent.com/s/lvu2v3583qxhk70/hapao%20matrix.png?dl=0" width="400">

* hapao again, will run the test again then will open the inspector with the hapao result.

## Built With

* [Roassal](http://agilevisualization.com/)
* [Pharo](http://pharo.org/)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
