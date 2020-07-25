# Firebase

Everything about Firebase in Swift

## Firestore

```swift
let db = Firestore.firestore()
```

### Adding data to Firestore

```swift

/// with custom id
db.collection("cities").document("new-city-id").setData(data)

/// with auto generated id
var ref: DocumentReference? = nil
ref = db.collection("cities").addDocument(data: [
    "name": "Tokyo",
    "country": "Japan"
]) { err in
    if let err = err {
        print("Error adding document: \(err)")
    } else {
        print("Document added with ID: \(ref!.documentID)")
    }
}
```