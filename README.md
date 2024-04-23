# Replicating Zod Error

Replicating the "Type instantiation is excessively deep and possibly infinite."
error when using Zod versions 3.23.0 and 3.23.1 with each other.

## Steps to Reproduce

1. Clone this repository
2. `npm install`
3. `npm start`

```bash
$ npm i

added 6 packages, and audited 7 packages in 3s

2 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

$ npm start

> zod-type-instantiation-error-replication@1.0.0 start
> rm -rf lib && tsc

src/index.ts:4:1 - error TS2589: Type instantiation is excessively deep and possibly infinite.

4 z_3_23_1.object({
  ~~~~~~~~~~~~~~~~~
5   str: z_3_23_0.string()
  ~~~~~~~~~~~~~~~~~~~~~~~~
6 })
  ~~


Found 1 error in src/index.ts:4
```
