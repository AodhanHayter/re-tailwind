# re-tailwind
ReasonML utility to generate Tailwind classes

## Install

```
npm install --save re-tailwind
```

Add re-tailwind to `bs-dependencies` in `bsconfig.json`

## Usage

1. Ensure your app already import tailwind css

```
[%bs.raw {|require("tailwindcss/dist/tailwind.min.css")|}];
```

2. Use function Tailwind.make to construct your tailwind classnames:

```
module Example = {
  [@react.component]
  let make = () =>
    <div className=Tailwind.make([`relative, `overflowHidden, `mbAuto])>
      {ReasonReact.string("Hello Example")}
    </div>;
};
```

## Credits
- [Typed tailwind](https://github.com/dvkndn/typed-tailwind) which has the same purpose to this project but in TypeScript

## License
[MIT](https://choosealicense.com/licenses/mit)
