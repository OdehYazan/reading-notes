# Forms and JS Events

[Reading-notes](https://odehyazan.github.io/reading-notes/)

## Forms

**Traditionally, the term 'form' has referred to a printed document that contains spaces for you to fill in information, but in HTML borrows the concept of a form to refer to different elements that allow you to collect information from visitors to your site.**

![form](https://img.webnots.com/2014/01/How-HTML-Form-Works.png)

### Form Controls

**ADDING TEXT:<br>1.Text input(single-line)<br>2.Password input<br>3.Text area (multi-line)**

**Making Choices:<br>1.Radio buttons<br>2.Checkboxes<br>3.Drop-down boxes**

**Submitting Forms:<br>1.Submit buttons<br>2.Image buttons**

**Uploading Files:<br>File upload**

***How forms work?***

 ![table1](../img/img37.jpg)

 **A form may have several form controls, each gathering different information. The server needs to know which piece of inputted data corresponds with which form element.**

 ### Form Structure

 **Form controls live inside a `<form>` element. This element should always carr the action attribute and will usually have a method and id attribute too.**

 **`action` Every `<form>` element requires an action attribute. Its value is the URL for the page on the server that will receive the information in the form when it is submitted.**

 **`method` Forms can be sent using one of two methods: `get` or `post`.**

 **`id`value is used to identify the form distinctly from other elements on the page(and is often used by scripts — such as those that check you have entered information into fields that require values).**

 ![table1](../img/img38.jpg)

#### Text Input

 ![text](https://miro.medium.com/max/5680/1*rnFktAV2cduHwin0hxN_dA.png)

#### Password Input

 ![pass](https://miro.medium.com/max/5756/1*1fVMQW2rMDXXAGaTdIOmyQ.png)

#### Checkbox, Radio  Input

 ![check](https://miro.medium.com/max/5760/1*5J2jxDwc3fkyBQ5C4XP4yw.png)

#### date,Email and Number Input

 ![check](https://miro.medium.com/max/5760/1*DkzUfKut64-XjrDABFsqrA.png)
