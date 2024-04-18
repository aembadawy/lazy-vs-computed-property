# lazy-vs-computed-property

## Lazy Variable

Lazy variable is only computed once when accessed. Perfect for use when the variable requires heavy computation.

## Computed Property

Computed property is recalculated each time it's accessed. And unlike *lazy var* they don't store the value. Instead they provide a getter and an optional setter to indirectly retrieve and set values.

| Lazy Variable | Computed Property |
| --- | --- |
| Deferred Initialization: They are initialized only once, and only when they are first accessed. | Dynamic Calculation: They recalculate their value every time they’re accessed. |
| Storage: After its initial calculation, the lazy variable retains its value and does not recompute. | No storage: Computed properties do not store the computed value. |
| Optimal for Expensive Operations | Reflect Changing State: Useful when the property value depends on other variables and can change over time. |
| Thread Safety Concerns: Lazy variables are not thread-safe by default, which means care must be taken when using them in a multithreaded context. | Thread Safety: Computed properties are just calculations and don’t have inherent thread safety issues, but the properties they rely on might. |


`Compasession base on meduim article` [here](https://mehrdad-ahmadian.medium.com/ios-interview-question-lazy-variables-vs-computed-properties-in-swift-b35fd323cbbd)
