//Crie um código JavaScript no back-end utilizando o Node.JS. No código, você deverá elaborar uma ou mais rotas, que podem ser de qualquer tipo (get, put etc). Depois, faça um teste em aplicações de rota, como o Postman ou o Insomnia, para confirmar se o retorno está coerente com o que você programou.

//Observação: os prints, ou o próprio código, devem ser divididos por arquivos. Por exemplo, o código de rotas está em um arquivo diferente do código de conexão.

//Código de conexão (arquivo "server.js"):

const express = require("express");
const app = express();

app.listen(3000, () => {
    console.log("Server running on port 3000");
});

//Código de rotas (arquivo "routes.js"):

const express = require("express");
const router = express.Router();

router.get("/", (req, res) => {
    res.send("Welcome to the home page!");
});

router.get("/about", (req, res) => {
    res.send("This is an example route for the about page.");
});

module.exports = router;

//Incluir as rotas no arquivo "server.js":

const routes = require("./routes");
app.use("/", routes);
