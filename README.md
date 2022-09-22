1. запрос(ы) для вставки данных минимум о двух книгах в коллекцию books

db.books.insertMany([
{title: "Квази", description: "роман", authors: "Сергей Лукьяненко"},
{title: "О дивный новый мир", description: "антиутопия", authors: "Олдос Хаксли"}
])

2. запрос для поиска полей документов коллекции books по полю title

db.books.find(
    {title: "Квази"}
)

3. запрос для редактирования полей: description и authors коллекции books по _id записи

db.books.UpdateOne(
  {_id: "objectId"},
  {
    $set: { 
        description: "Новое описание", 
        authors: "Новый автор" 
    } 
  }
)