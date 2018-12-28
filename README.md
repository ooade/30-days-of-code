# 30-days-of-code
Daily log of the things I read and learn during week days, and maybe weekends.
This may include stuffs on web performance, css, javascript, accessibility, reactjs and golang :)

### 27/12/2018
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


### 28/12/2018
#### Golang
Resource: [The go programming language](https://www.gopl.io/)
- I learnt about the bufio package. Providing seamless way to read inputs from the os stdin.
- The map function; a key-value pair data structure.
- The make function, which seem to define how the map function would be; will be explained in a later chapter.
- fmt.Printf; Although, it's the same as in C, but just found out it's also available in go.
