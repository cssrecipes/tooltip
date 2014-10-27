# Tooltip

> Simple tooltip using an html attribute for the content

## Install

```sh
$ npm install cssrecipes-tooltip
```

## Usage

Example:

```html
<span class="cssr-Tooltip cssr-Tooltip--bottom" data-cssr-tooltip="I'm the tooltip body">Hover me to see the tooltip !</span>
```

## Available classes

### `.cssr-Tooltip`

#### Position modifiers

##### `.cssr-Tooltip--top`
##### `.cssr-Tooltip--bottom`
##### `.cssr-Tooltip--left`
##### `.cssr-Tooltip--right`

#### Visibility modifier

##### `.cssr-Tooltip--visible`

Force visibility (no need to hover).

##### `.cssr-Tooltip--nowrap`

Add a avoid whitespace to wrap content (force content to be on one line).

##### `.cssr-Tooltip--centerText`

Add `text-align: center` on the tooltip content.


## Availables custom properties

```css
:root {
	--cssr-Tooltip-zIndex: 1000;
	--cssr-Tooltip-backgroundColor: #383838;
	--cssr-Tooltip-margin: .5rem;

	--cssr-Tooltip-arrow-size: .5rem;
}
```

## Customize

If custom properties are not enough, you can obviously override default rules. Or add modifier(s).

### Adding a state

It's easy to add a `success` or `error` state.

```css
.cssr-Tooltip--STATE::before {
	background-color: var(--cssr-Tooltip--STATE-color);
	text-shadow: 0 -1px 0 color(var(--cssr-Tooltip--STATE-color) blackness(90%));
}
	.cssr-Tooltip--STATE.cssr-Tooltip--top::after { border-top-color: var(--cssr-Tooltip--STATE-color) }
	.cssr-Tooltip--STATE.cssr-Tooltip--bottom::after { border-bottom-color: var(--cssr-Tooltip--STATE-color) }
	.cssr-Tooltip--STATE.cssr-Tooltip--left::after { border-left-color: var(--cssr-Tooltip--STATE-color) }
	.cssr-Tooltip--STATE.cssr-Tooltip--right::after { border-right-color: var(--cssr-Tooltip--STATE-color) }
```

---

## Testing

To generate a build:

```sh
$ npm run build
```

To generate the testing build.

```sh
$ npm run build-test
```

Basic visual tests are in `test/index.html`.

## Contributing

Work on a branch, install dev-dependencies, respect coding style & run tests before submitting a bug fix or a feature.

```sh
$ git clone https://github.com/cssrecipes/tooltip.git
$ git checkout -b patch-1
$ npm install
$ npm test
```

## [Changelog](CHANGELOG.md)

## [License](LICENSE)
