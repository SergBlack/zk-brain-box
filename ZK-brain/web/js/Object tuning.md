202203272226
Tags: #javascript 

--- 
# Object "tuning"
Property tuning (setting descriptors manually):
- `Object.defineProperty`
- `Object.defineProperties`
- `Object.getOwnPropertyDescriptor` - allows you to get complete information about the property
- `Object.getOwnPropertyDescriptors` - allows you to get complete information about all properties

Object tuning (setting descriptors with provided methods):
- `Object.preventExtensions` - prevent adding a new property
- `Object.seal` - can change value, but prevent adding a new property and configure decriptors
- `Object.freeze` - prevent any changes to the object and configure decriptors (the hardest way)

Check if object is configured with provided methods:
- `Object.isExtensible`
- `Object.isSealed`
- `Object.isFrozen`

--- 
### Links
- [[Descriptors]]