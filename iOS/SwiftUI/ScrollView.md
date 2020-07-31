# ScrollView

## Detecting if you're scrolling up or down

```swift
.gesture(DragGesture().onChanged { value in
                    if value.translation.height > 0 {
                       print("Scroll down")
                    } else {
                       print("Scroll up")
                    }
                })
```