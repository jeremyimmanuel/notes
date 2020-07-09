# React Native Core Components

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
