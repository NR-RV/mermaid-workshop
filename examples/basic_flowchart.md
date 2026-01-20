# Basic Flowchart Example

Flowcharts are used to represent workflows or processes. They show steps as boxes of various kinds, and their order by connecting them with arrows.

## Simple Flowchart

```mermaid
flowchart TD
    A[Start] --> B{Is it working?}
    B -->|Yes| C[Great!]
    B -->|No| D[Debug]
    D --> B
    C --> E[End]
```

## Flowchart with Different Shapes

```mermaid
flowchart LR
    A[Square] --> B(Rounded)
    B --> C{Diamond}
    C -->|Option 1| D[Result 1]
    C -->|Option 2| E[Result 2]
```

## Resources

- [Mermaid Flowchart Documentation](https://mermaid.js.org/syntax/flowchart.html)
