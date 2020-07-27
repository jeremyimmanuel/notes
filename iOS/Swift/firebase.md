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

### Queries

```swift
let db = Firestore.firestore()

// Let's say we have a colletions of users
let usersCollection = db.collection("users")

// Assume doc id is "apple"
let docRef = usersCollection.document("apple") // DocumentReference
```

After this step you got `docRef` which is an object of type [DocumentReference](https://firebase.google.com/docs/reference/swift/firebasefirestore/api/reference/Classes/DocumentReference). 

We still need to call the object's `.getDocument` function to get the data in a form of a dictionary.

```swift
docRef.getDocument { document, error in
if let document = document, document.exists {
    document.data() // the dictionary
}
```