---
title: My Introduction Page
---

# Top Level Heading
Displays HTML properly
<button class="btn btn-primary">Test Button</button>

## My CodeBlock Component
I would like it to display the HTML code instead of parsing it and displaying the button
<CodeBlock language="html">
  <button>Test Button</button>
</CodeBlock>

This style of code block is also acceptable but I would like it to have code highlighting
```
  <button>Test Button</button>
```

CodeBlock works with javascript

<CodeBlock language="javascript">
function doTheThing(theThing) {
  doIt(theThing)
    .then(done =>{
      console.log(`This thing has been done. ${done}`);
    }) 
    .catch(error => {
      console.log(`The thing failed ${error.message}`);
    });
}
</CodeBlock>

## Playing with other style of components
<Color name="$chGreen" hex="#1a1a1a"/>
<Color name="$chGrey" hex="#CCC"/>