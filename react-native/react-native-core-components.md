# React Native Core Components

List of react native core components

## Button

```jsx
<Button 
    title=”Change Text” 
    onPress={() => setOutputText(‘The text changed!’)}/>
```

## Scroll View

```jsx
<ScrollView horizontal>
    {
        courseGoals.map((goal) => 
            <View style={styles.listItem}>
                <Text key={goal}>{goal}</Text>
            </View>)
    }
</ScrollView>
```

## Flat List

Similar to ScrollView but builds the list dynamically

```jsx
<FlatList
    // keyExtractor = {(item, index) => item.key}
    data={courseGoals}
    renderItem={
    itemData => (
        <View style={styles.listItem}>
        <Text>{itemData.item.value}</Text>
        </View>
    )
}/>
```

## Alert Dialog

We can show alert dialog via a function.
For further information look [here](https://reactnative.dev/docs/alert).

```javascript
Alert.alert(
      "Alert Title",
      "My Alert Msg",
      [
        {
          text: "Cancel",
          onPress: () => console.log("Cancel Pressed"),
          style: "cancel"
        },
        { text: "OK", onPress: () => console.log("OK Pressed") }
      ],
      { cancelable: false }
    );

```
