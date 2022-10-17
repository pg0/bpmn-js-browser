catch event bus

``` js

var eventBus = bpmnModeler.get('eventBus');

// you may hook into any of the following events
var events = [
  'element.hover',
  'element.out',
  'element.click',
  'element.dblclick',
  'element.mousedown',
  'element.mouseup'
];

events.forEach(function(event) {

  eventBus.on(event, function(e) {
    // e.element = the model element
    // e.gfx = the graphical element

    console.log(event, 'on', e.element.id);
  });
});


```