# Debug area

- This container can be used to inspect the space taken by its children.
- The `DebugArea` container does not alter a document's layout.

```csharp
// You can specify text and color,
// to better distinguish between various debug elements:
.DebugArea("Grid example", Colors.Blue.Medium)

// You can skip the color. By default it is red:
.DebugArea("Grid example")

// Or use default style:
.DebugArea()
```

Example:

```csharp{4}
container
    .Padding(25)
    .DebugArea("Grid example", Colors.Blue.Medium)
    .Grid(grid =>
    {
        grid.Columns(3);
        grid.Spacing(5);

        foreach (var _ in Enumerable.Range(0, 8))
            grid.Item().Height(50).Placeholder();
    });
```

![example](/api-reference/debug.png =420x)
