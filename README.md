import { Card } from "react-bootstrap";
import product from "./product";
import Name from "./Name";
import Price from "./Price";
import Description from "./Description";
import Image from "./Image";

function App() {
  const firstName = "John"; // Change to "" to test "Hello, there!"

  return (
    <div className="d-flex flex-column align-items-center p-4">
      <Card style={{ width: "22rem" }} className="shadow-lg">
        <Card.Body className="text-center">
          <Image image={product.image} alt={product.name} />
          <Name name={product.name} />
          <Price price={product.price} />
          <Description description={product.description} />
        </Card.Body>
      </Card>

      <div className="mt-3 text-center">
        {firstName ? (
          <>
            <h3>Hello, {firstName}!</h3>
            <img
              src="https://via.placeholder.com/100"
              alt="User avatar"
              className="rounded-circle mt-2"
            />
          </>
        ) : (
          <h3>Hello, there!</h3>
        )}
      </div>
    </div>
  );
}

export default App;
