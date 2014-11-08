# Tooltip

> Simple tooltip using an html attribute for the content

## Install

```sh
$ npm install cssrecipes-tooltip
```

## Usage

Example:

```html
<span class="r-Tooltip r-Tooltip--bottom" data-r-tooltip="I'm the tooltip body">Hover me to see the tooltip !</span>
```

## Available classes

### `.r-Tooltip`

#### Position modifiers

##### `.r-Tooltip--top`
##### `.r-Tooltip--bottom`
##### `.r-Tooltip--left`
##### `.r-Tooltip--right`

#### Visibility modifier

##### `.r-Tooltip--visible`

Force visibility (no need to hover).

##### `.r-Tooltip--nowrap`

Add a avoid whitespace to wrap content (force content to be on one line).

##### `.r-Tooltip--centerText`

Add `text-align: center` on the tooltip content.


## Availables custom properties

```css
:root {
	--r-Tooltip-zIndex: 1000;
	--r-Tooltip-backgroundColor: #383838;
	--r-Tooltip-margin: .5rem;

	--r-Tooltip-arrow-size: .5rem;
}
```

## Customize

If custom properties are not enough, you can obviously override default rules. Or add modifier(s).

### Adding a state

It's easy to add a `success` or `error` state.

```css
.r-Tooltip--STATE::before {
	background-color: var(--r-Tooltip--STATE-color);
	text-shadow: 0 -1px 0 color(var(--r-Tooltip--STATE-color) blackness(90%));
}
	.r-Tooltip--STATE.r-Tooltip--top::after { border-top-color: var(--r-Tooltip--STATE-color) }
	.r-Tooltip--STATE.r-Tooltip--bottom::after { border-bottom-color: var(--r-Tooltip--STATE-color) }
	.r-Tooltip--STATE.r-Tooltip--left::after { border-left-color: var(--r-Tooltip--STATE-color) }
	.r-Tooltip--STATE.r-Tooltip--right::after { border-right-color: var(--r-Tooltip--STATE-color) }
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
