# fastui-carousel
react-native轮播图组件

## Demo
![](https://raw.githubusercontent.com/roscoe054/fastui-carousel/master/demo.gif)

## Install
```
npm install fastui-form
```

## Example
```javascript
'use strict';

import React, {AppRegistry, Component, StyleSheet, Dimensions, Text, View, Image, StatusBarIOS} from 'react-native';

var Carousel = require('./fastui-carousel');

var CarouselDemo = React.createClass({
    componentWillMount() {
        StatusBarIOS.setHidden(true)
    },
    render() {
        return (
            <View style={styles.container}>
                <Carousel>
                    <View style={styles.page}>
                        <Image
                            style={styles.img}
                            source={{uri: 'http://7xkm02.com1.z0.glb.clouddn.com/page1.png'}}
                        />
                    </View>
                    <View style={styles.page}>
                        <Image
                            style={styles.img}
                            source={{uri: 'http://7xkm02.com1.z0.glb.clouddn.com/page2.png'}}
                        />
                    </View>
                    <View style={styles.page}>
                        <Image
                            style={styles.img}
                            source={{uri: 'http://7xkm02.com1.z0.glb.clouddn.com/page3.png'}}
                        />
                    </View>
                </Carousel>
            </View>
        );
    }
});

const styles = StyleSheet.create({
    container: {
        flex: 1,
    },
    page: {
        width: Dimensions.get('window').width,
        flex: 1,
        alignItems: 'stretch',
    },
    img: {
        flex:1,
    },
});

AppRegistry.registerComponent('CarouselDemo', () => CarouselDemo);
```
