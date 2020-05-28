= Selectors =
selector {
  property: value;
  property: value;
}

- inline styles (style attribute on element)
- internal styles (embedded style sheet via style tag)
- external styles (<link href="path/to/file.css" rel="stylesheet">)

- type selector : like div, targets a specific type of HTML element
- class selector : uses when multiple page objects require same styling
  <element class="class-name">
  class names are case-sensitive

  .class-name {
   property: value;
  }

  You can apply multiple classes to a single element by separating class names with a space.
