<pre>


  import React from "react";
import ReactDom from "react-dom/client";

import "./index.css";

// const BookList = () => {
//   return <section className="Booklist">
//     <Book name={FirstBook.name} author={FirstBook.author} img={FirstBook.img}> 
//       <p>
//           sadsadsadsa
//       </p>
//       <button>click me</button>

//     </Book>
//     <Book name={SecondBook.name} author={SecondBook.author} img={SecondBook.img} />
//     <Book name={ThirdBook.name} author={ThirdBook.author} img={ThirdBook.img} />
//   </section>;
// }


const BookList = () => {
  return <section className="Booklist">
    {allbooks.map((book) => {
      return <Book key={book.name} name={book.name} author={book.author} img={book.img} />
    })}
  </section>;
}

const fontcolor = {
  color: "red"
}


const allbooks = [
  {
    name: "The way of kings",
    author: "Brandon Sanderson",
    img: "https://images-na.ssl-images-amazon.com/images/I/51N-u8AsmdL._SX258_BO1,204,203,200_.jpg"
  },
  {
    name: "Justinian",
    author: "Robert Graves",
    img: ""
  },
  {
    name: "and then there were none",
    author: "Agatha Christie",
    img: "https://images-na.ssl-images-amazon.com/images/I/51N-u8AsmdL._SX258_BO1,204,203,200_.jpg"
  }
]

const Book = ({ name, author, img , children}) => {
  console.log({ name, author, img });
  return <article className="Book">
    <img src={img} alt="book" />
    <h3 style={fontcolor}> {author} </h3>

    <p> {name} </p>
    {children}
  </article>;
}

const Titlw = "The way of kings";
const AuthorName = "Brandon Sanderson";


// const Image = () => <img src="https://images-na.ssl-images-amazon.com/images/I/51N-u8AsmdL._SX258_BO1,204,203,200_.jpg" alt="book" />;
// const Title = () => <h3 style={fontcolor}>{Titlw}</h3>;
// const Author = () => <p style={fontcolor}>{AuthorName}</p>;

const root = ReactDom.createRoot(document.getElementById("root"));
root.render(<BookList/>);
</pre>
