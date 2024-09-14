# What is Indexed Types in Typescript?

Indexed types allows you to query the type of a specific property from another
type. They are useful when accessing array/tuple values, object values, and more.

> In case of literal array/tuple/object values, it evaluates the literal value itself
> but for a string literal, it will return 'string' for any character accessed.

```ts
type Cars = ['Bugatti', 'Ferarri', 'Lambo', 'Porsche', 'Toyota Corolla'];
type SecondCar = Cars[1]; // 'Ferarri'

type Donations = {
  Bono: 15_000_000;
  'J.K. Rowling': 160_000_000;
  'Taylor Swift': 45_000_000;
  'Elton John': 600_000_000;
  'Angelina Jolie and Brad Pitt': 100_000_000;
};
type EltonDonations = Donations['Elton John']; // 600_000_000

type Statement = 'Hello World!'
type FirstCharacter = Statement[0] // string
```
