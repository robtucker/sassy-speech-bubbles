# Speech Bubbles for Bootstrap 3

Example: 

```<div class="speech-bubble speech-bubble-testimonial-sm"></div>```

### Taking the hassle out of the triangle bit

The problem with speech bubbles is the little triangle bit that sticks out of the side - the bit which points at the mouth of the person who is speaking.

Consider a situation where the layout changes between different screen sizes and then the triangle needs to be in a completely different place altogether.

This repo offers a quick suggestion for how you might generate css speech bubbles on the fly using Sass. Using the speech bubble mixin provided, you can quickly tweak all of the parameters that go into creating your speech bubble.

Because of this it is also pretty easy to generate a speech bubble class that has one position for small devices and another position for large devices.


### Usage

to create a speech bubble class simply follow the example:

```
.speech-bubble-testimonial-left {
    @include speech-bubble-triangle('top', 1px, $gray-border-light, 15px, 15px, 50%);
}
```

The arguments:

1. which side of the parent div to put the triangle on,
2. border width 
3. border color
4. length of triangle bit
5. width of triangle bit
6. the position of the triangle on the speech bubble as a %. So 50% would mean the triangle is in the middle of the speech bubble (on whichever side you choose)


Obviously it should be pretty easy to customize these mixins with your own logic, such as broder radius etc etc.

Finally - it should be easy to adapt these for bootstrap 4, or any framework. I just happen to have used the grid breakpoints from bootstrap 3.

Hope this approach helps someone else out.

