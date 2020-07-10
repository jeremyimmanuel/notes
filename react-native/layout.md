# Layout

By default, every component uses flexbox as it's method of layouting.

```jsx
<View styles>

</View>

const styles = StyleSheet.create({
    container: {
        flex: 1, // will make view follow the size of parent, if not set then view will just fill as needed (follow its children)
        padding: 10,
        justifyContent: 'center', // main - axis alignment
        alignItems: 'center', // cross-axis alignment
        width: '60%', // when doing percentage, it means a percentage of its parent's length
    }
})
