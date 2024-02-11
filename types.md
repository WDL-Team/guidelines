# Typescript guidelines

Try to avoid using 'as'.
Never use 'any'.

Remember to use 'readonly' keyword in front of the property name. Use this for properties that should only be modified when an object is first created.

Remember to use 'enum' primitive type. Use this to declare persistent names for properties that may change their value during development.

## Interface / Type

Interfaces should not start with the letter I, interface names are in PascalCase.

Types must start from letter T, type names are in TPascalCase.

While defining type of props avoid using just a TProps. Name must always contain information what exactly props you are defining. Example: TButtonProps.
 
You can define a function type using a type alias or an interface. Both approaches work essentially the same so it's up to you to decide which is best. An interface is better if you want to have the option of extending the function type. A type alias is better if you want to use unions or tuples.
Use 'interface' to define extendable set of properties and 'type' for the constant ones.

When extending an interface with one or more interfaces, these rules apply:
- You must implement all the required properties from all interfaces.
- Two interfaces can have the same property if the property has the exact same name and type.
- If two interfaces have a property with the same name but different types, you must declare a new property such that the resulting property is a subtype of both interfaces.

Итого: функции, классы, компоненты декларируем interface-ами, объекты и пропсы type-ами. Не плодим схожие декларирования, если их можно описать дженериками. ( специально выделил самую важную часть :)
