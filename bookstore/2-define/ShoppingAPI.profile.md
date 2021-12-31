# Shopping API

* Supports the book browsing experience and cart management
* Scope: Public


# API Product profile

| No| Aspect         | Description     |
|-- |--------------|-----------|
|1| API consumers| Developers building affiliate mobile bookshop applications. |
|2| Core benefit| Supports the book browsing experience and cart management.|
|3| Business capabilities| 1) Send messags  2) Receive messages 3) Manage contacts 4) Query metadata information on sent and received messags 5) Create message templates|
|4| API product manger      | John Smith |
|5| API solution | REST API. Connects to the Messaging, Contacts, Notification and Template microservices. | 
|6| Usage and pricing plans | £0.03 per text message sent.| 
|7| Documentation and support |Available at developer.acmemessaging.com | 
|8| API product KPIs | 1) Number of sent text messages 2) Monthly active users 3) API usage growth  | 
|9| Security model| OAuth 2.0|
|10| Access level | Public |


# API interface profile

| Operation Name       | Description                               | Participants          | Resource(s)       | Emitted Events   | Operation Details                                                          | Traits                     |
|----------------------|-------------------------------------------|-----------------------|-------------------|------------------|----------------------------------------------------------------------------|----------------------------|
| listBooks()          | List books by category or release date    | Customer, Call Center | Book, Book Author | Books.Listed     | __Request Parameters:__ categoryId, releaseDate     __Returns:__   Books[] | safe   / synchronous       |
| searchBooks()        | Search   for books by author, title       | Customer, Call Center | Book              | Books.Searched   | __Request Parameters:__ searchQuery     __Returns:__   Books[]             | safe   / synchronous       |
| addItemToCart()      | Add a book to the customer's cart         | Customer, Call Center | Cart Item, Cart   | Cart.ItemAdded   | __Request Parameters:__ cartId, bookId,   quantity     __Returns:__   Cart | unsafe   / synchronous     |
| removeItemFromCart() | Remove a book from the customer's cart    | Customer, Call Center | Cart Item, Cart   | Cart.ItemRemoved | __Request Parameters:__ cartItemId     __Returns:__   Cart                 | idempotent   / synchronous |
| clearCart()          | Remove all books from the customer's cart | Customer, Call Center | Cart              | Cart.Cleared     | __Request Parameters:__ cartId     __Returns:__   Cart                     | safe / synchronous         |
| viewCart()           | View   the current cart and total         | Customer, Call Center | Cart              | Cart.Viewed      | __Request Parameters:__ cartId     __Returns:__   Cart                     | safe / synchronous         |
