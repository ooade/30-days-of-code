# 30-days-of-code
Daily log of the things I read and learn during week days, and maybe weekends.
This may include stuffs on web performance, css, javascript, accessibility, reactjs and golang :)

### Day 1: 27/12/2018
#### Golang
Resource: [The go programming language](https://www.gopl.io/)
- I learnt about the short hand variable declaration in go (`i := "some value"`)
- The os package. With this you can get the list of arguments from the command line using `os.Args`
- The range method. Applied to `os.Args`, you'll get `index` and `value`.
- A cool one from the strings package(`strings.Join`). Short and precise :)

#### Performance
Resource: [What is first input delay](https://bitsofco.de/what-is-first-input-delay/)
- Hot one from Ire. FID metric is like the intersection between FCP(The time content starts to show on the webpage) and FMP(The time you have meaningful content on the page).
- It's more like the time one will be able to use form inputs on the page.
- The library; [FID](https://github.com/GoogleChromeLabs/first-input-delay) - used for deriving FID perf metrics.

#### Chrome Dev Summit Highlight
Resource: [Highlights from Chrome Dev Summit 2018](https://bitsofco.de/chrome-dev-summit-2018/)
- [Squoosh](https://squoosh.app/) - A 15kb JS-powered web application.
- Page Speed. I was only aware of lighthouse.
- Native lazyloading in Chrome. Yeah, Chrome is finally supporting this using the scroll to load method.
- Portal - Seemless Navigation transitions like native applications. It really is a nice prosposal.


### Day 2: 28/12/2018
#### Golang
Resource: [The go programming language](https://www.gopl.io/)
- I learnt about the bufio package. Providing seamless way to read inputs from the os stdin.
- The map function; a key-value pair data structure.
- The make function, which seem to define how the map function would be; will be explained in a later chapter.
- fmt.Printf; Although, it's the same as in C, but just found out it's also available in go.

#### React Internals
Resource: [How react tells a class from a function](https://overreacted.io/how-does-react-tell-a-class-from-a-function/)
- I learnt it adds isReactComponent to React Component's prototype to achieve this.
- The error it gives out if one do not extend React Component, and how it knows it should extend it. That is, checking if a render function exists.
- Several other ways one might want to approach checking the two.

#### Performance
Resource: [Understanding the critical rendering path](https://bitsofco.de/understanding-the-critical-rendering-path/)
- I learnt about the various CRP stages.
- I learnt a little bit about CSSOM.

#### Javascript
Resource: [Web workers vs Service Workers vs Worklets](https://bitsofco.de/web-workers-vs-service-workers-vs-worklets/)
- I already knew what web workers and service workers are, and how they work. Worklet was a new thing to me here.
- With worklet, you can hook into the various part of the rendering process and add some custom style or something.
- I learnt about the paint worklet, and there are others like the layout worklet and the animation worklet.

### Day 3: 29/12/2018
#### Performance
Resource: [Why and how to use webp images today](https://bitsofco.de/why-and-how-to-use-webp-images-today/)
- Webp images are awesome. Supports lossless and lossy compressions, can be animated, and supports transparency.
- It was created by Google.
- It's supported in over 70% of browsers today.
- Squoosh can also convert to webp.

#### Golang
Resource: [Go lang Tour](https://tour.golang.org)
- Go can return multiple results. It literally blew my mind.
- Modules (math/rand, math/complex). They'll still be written as rand.Method and complex.Method.
- Type conversion. int(3.39), and so on.

### Day 4: 31/12/2018
#### Golang
Resource: [Go lang Tour](https://tour.golang.org)
- The newton's method for solving sqrt `z -= (z * z - x) / (2 * z)`
- Switch statements in Go do not require a break.
- The [time package](https://golang.org/pkg/time/). `time.Now()`, `time.Now().Weekday()` and so on...
- A switch statement may take no conditions :)
- The `defer` statement. Cool one!!!!!!
- Stacking defer statements. Like in a loop. The last value shows off before the first :( :)

### Day 5: 1/1/2019
#### Golang
Resource: [Go lang Tour](https://tour.golang.org)
- Pointers: Almost the same as C. Type can also be a pointer type, like `*int`.
- Struct. Almost also like the one in C. Except that using the struct here is different.
More like:
```go
StructName{Set of Values}
```
- Arrays. 
- Slices - Using colons to specify the low and high bound.
- Length `len`, and Capacity `cap` in slices.

#### Fun stuff
Resource: [Using a headless browser to capture page screenshots](https://bitsofco.de/using-a-headless-browser-to-capture-page-screenshots/)
- I got to learn about puppeteer, even while I think that `browser.newPage` is a bad API design as opposed to `browser.newTab`.

### Day 6: 2/1/2019
#### Javascript
Resource: [10 Interview questions every javascript developer should know]https://medium.com/javascript-scene/10-interview-questions-every-javascript-developer-should-know-6fa6bdf5ad95
- Relearnt [OOLO and Prototype design pattern](https://stackoverflow.com/questions/29788181/kyle-simpsons-oloo-pattern-vs-prototype-design-pattern).
- Relearnt what first class functions are. Functions in javascripts are said to be first class functions because they are treated like other variables.
- Relearnt [anonymous functions and lambdas](https://gist.github.com/ericelliott/414be9be82128443f6df). BTW, lambas are functions used as data.
- Favoring object composition over class inheritance; Avoids tight coupling, class hierachies, and rigid taxonomy(forced is-a relationship). Gorilla banana problem too :)
- Relearnt one-way data binding(as done in React/Redux) as opposed to two-way data binding(Angular). One-way data binding are deterministic.
- Monolithic vs Microservices; Sigh. Monolithic is like having the whole codebase as one unit, sharing same memory space and resources. Microservices: seperate servers handling unique jobs.
- Async Javascript: Sync blocks the thread until the resource is returned as opposed to async.


#### Golang
Resource: [Go lang Tour](https://tour.golang.org)
- Creating a slice with make. I actually don't know why you'd prefer this method except explicitly providing the length and capacity of the slice respectively in the `make` function

### Day 7: 3/1/2019
#### Javascript
Resource: [What exactly is the DOM](https://bitsofco.de/what-exactly-is-the-dom/)
- The combination of the DOM and CSSOM forms the render tree.
- The DOM doesn't include psuedo-elements.

#### Golang
Resource: [Go lang Tour](https://tour.golang.org)
- I did the slice exercise and also joined folks in posting the [solution](https://gist.github.com/tetsuok/2280162#gistcomment-928498) :sweat_smile:

### Day 8: 4/1/2019
#### Golang
Resource: [Go lang Tour](https://tour.golang.org)
- Map and make map :)
- Map literals
- I learnt how to check if a key exist like
```go
  v, ok := m["Answer"]
```
- `string.Fields` to split string into fields, like javascript `String.prototype.split`.
- I solved the Maps exercise using what I had learnt previously (make, map, strings.Field, for, if).
- Function as values.
- Function closures. I played around with this for a while. Created 3 nested FoF :zap:
- Fabonacci Exercise
```go
  func fibonacci() func() int {
    a, b := 0, 1

    return func() int {
      defer func() {
        a, b = a + b, a
      }()

      return a
    }
  }
```

#### GIT Hacks
Resource: [GIT aliases for lazy developers](https://bitsofco.de/git-aliases-for-lazy-developers/)
- I set up some aliases on my fish terminal using `alias` command and `funcsave`

### Day 8: 5/1/2019
#### Golang
Resource: [Go lang Tour](https://tour.golang.org)
- Methods in go. Methods are functions with a receiver argument.
- Defining methods on non struct types.
- Pointers receivers.
- Indirect pointers by setting the type as pointer `v := &Vertex{2, 3}`.
- Interfaces.

#### CSSOM
Resource: [An Introduction and guide to the css object model](https://css-tricks.com/an-introduction-and-guide-to-the-css-object-model-cssom)
- Read only `window.getComputedStyle(elementSelector, ?pseudoElement)`
- Getting the style property off an elementSelector. As in: `document.body.style.backgroundColor`. I.e if previously declared as style.
- Or getting it via `document.body.style.getPropertyValue(property)` and `document.body.style.setProperty(property, value)`.
- `....style.removeProperty(propertyName)`.
- `....style.item(index)`. I don't see how much this is relevant tho :(
- `....style.getPropertyPriority` - To see if the property has the important flag.
- The CSSStyleSheet Interface.
- Types in CSSRules. Yeah, freaking awesome. Type 1 specifies styles, `IMPORT_RULE (3), MEDIA_RULE (4), KEYFRAMES_RULE (7)`. The rest can be gotten [here](https://developer.mozilla.org/en-US/docs/Web/API/CSSRule#Type_constants).
- Get `conditionText` from type `4 (MEDIA RULE)` of `cssRules`
- Values can be set to the `cssRules`.
- More and more types were discussed with various way of getting values.
- InsertRule. `document.styleSheets[0].insertRule(string of rule, where it should be added, defaults to 0)`.
- DeleteRule. `document.styleSheets[0].deleteRule(index)`.


### Day 9: 6/1/2019
#### Golang
Resource: [Go lang Tour](https://tour.golang.org)
- Nil interface values.
- Empty interfaces. Holds values of unknown types.


### Day 10: 7/1/2019
#### Golang
Resource: [Go lang Tour](https://tour.golang.org)
- Type assertions. `t := i.(T)`
- Type switches. Respond differently based on the type.
- Stringers. Nice way to format an output based on an interface


### Day 11: 8/1/2019
#### Golang
Resource: [Go lang Tour](https://tour.golang.org)
- Did the Stringer exercise. It all makes sense now
```go
package main

import (
	"fmt" 
	"strings"
	)

type IPAddr [4]byte

func (ip IPAddr) String() string {
	r := make([]string, len(ip))

	for i, val := range ip {
		r[i] = fmt.Sprintf("%v", int(val))
	}

	return strings.Join(r, ".")
}

func main() {
	hosts := map[string]IPAddr{
		"loopback":  {127, 0, 0, 1},
		"googleDNS": {8, 8, 8, 8},
	}
	for name, ip := range hosts {
		fmt.Printf("%v: %v\n", name, ip)
	}
}
```

- Errors, and its interface.
