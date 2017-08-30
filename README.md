## react-native-view-more-text

A super lightweight plugin to expand/collapse text in React-Native. Truncated text is ended with dotdotdot.

Working on IOS/Android

![ios](https://raw.githubusercontent.com/guilhermepontes/react-native-view-more-text/master/ios.gif)
![android](https://raw.githubusercontent.com/guilhermepontes/react-native-view-more-text/master/android.gif)

### Installation

```
yarn add react-native-view-more-text
npm install --save react-native-view-more-text
```

### Usage

- **numberOfLines**(required): Number of lines to be displayed.
- **renderViewMore**: Render view-more component
- **renderViewLess**: Render view-less component
- **afterCollapse**: Callback after collapsing
- **afterExpand**: Callback after expanding

```jsx
import React, { Component } from 'react';
import { Text } from 'react-native';
import ViewMoreText from 'react-native-view-more-text';

class Example extends Component {
  renderViewMore = onPress => <Text onPress={onPress}>View more</Text>
  renderViewLess = onPress => <Text onPress={onPress}>View less</Text>

  render() {
    return (
      <ViewMoreText
        numberOfLines={3}
        renderViewMore={this.renderViewMore}
        renderViewLess={this.renderViewLess}
      >
        <Text>
          Lorem ipsum dolor sit amet, in quo dolorum ponderum,
          nam veri molestie constituto eu. Eum enim tantas
          sadipscing ne, ut omnes malorum nostrum cum. Errem
          populo qui ne, ea ipsum antiopam definitionem eos.
        </Text>
      </ViewMoreText>
    )
  }
}
```
