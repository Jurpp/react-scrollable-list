# React Scrollable List

## Render your own component

This fork makes it possible to pass your own component rendering function.

## React scrollable list

React Scrollable List is a scrollable, high-performance list component for
rendering large lists of items with React. It's performance really shines when
dealing with lists in excess of a thousand items, and scales well into the
millions or more. Due to it only rendering a small slice of the list into the
DOM at any time based on the scroll position, it removes most of the speed
issues with web browsers and rendering very large amounts of DOM nodes at once.

To style the elements you can simply refer to the `.react-scrollable-list` class.
The component takes up to four props:

- listItems: an array of items in the format specified above
- heightOfItem: the CSS height of each item (needs to be the same for each item)
- renderListItem:
- maxItemsToRender: an optional number which tells the component how many components before and after the item scrolled to it should pre-render
- style: an optional style object to add inline styling through JS

```js
<ReactScrollableList
  listItems=[...]
  heightOfItem={30}
  renderListItem={(item) => <MyComponent data={item}>}
  maxItemsToRender={50}
  className={'my-css-classname'}
  style={{ color: '#333' }}
/>
```

## Notes

To build a CommonJS version of this file simply run `npm run build`.
A build is already included in the dist folder.

## License

[MIT](./LICENSE)
