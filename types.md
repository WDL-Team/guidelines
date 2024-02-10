Interfaces should not start with the letter I, interface names are in PascalCase.

Types must start from letter T, type names are in TPascalCase.

While defining type of props avoid using just a TProps. Name must always contain information what exactly props you are defining. Example: TButtonProps.
 
Use 'interface' to define extendable set of properties and 'type' for the constant ones.
 
Try to avoid using 'as'.
Never use 'any'.

Remember to use 'readonly' keyword in front of the property name. Use this for properties that should only be modified when an object is first created.

Remember to use 'enum' primitive type. Use this to declare persistent names for properties that may change their value during development.

When extending an interface with one or more interfaces, these rules apply:
- You must implement all the required properties from all interfaces.
- Two interfaces can have the same property if the property has the exact same name and type.
- If two interfaces have a property with the same name but different types, you must declare a new property such that the resulting property is a subtype of both interfaces.
