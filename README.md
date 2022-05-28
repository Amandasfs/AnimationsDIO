#README
<div class="container">
        <div class="card">
            <div class="card-wrapper">
                <h2>Github</h2>
                <p>Bem Vindos! Aqui estão alguns de meus projetos, espero que gostem!</p>
            </div>
        </div>
</div>
.container{
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}
.card{
    height: 400px;
    width: 500px;
    background-image: url(./Img/imagem-background.jpg);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover; /*Faz com que a Imagem cubra todo o bloco*/
    display: flex;
    justify-content: center;
    align-items: center;
    filter: grayscale(0.5);
    color: #e29eff;
    cursor: pointer;
    transition: 0.3s;
}
.card-wrapper{
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: relative;
}
.card-wrapper::before{
    content: '';
    position: absolute;
    height: 100px;
    width: 100px;
    display: block;
    border: 1px solid #eeccfc;
    opacity: 0;
    transition: 0.3s;
}
.card-wrapper h2{
    font-size: 40px;
    text-transform: uppercase;
    letter-spacing: 4px;
    margin: 0;
    transition: 0.3s;
}
.card-wrapper p{
    font-size: 0;
    visibility: hidden;
    opacity: 0;
    font-weight: bold;
    text-transform: uppercase;
    transition: 0.3s;
}
.card:hover{
 filter: unset;
}
.card:hover > .card-wrapper::before{
    height: 300px;
    width: 400px;
    opacity: 1;
}
.card:hover > .card-wrapper p {
    opacity: 1;
    visibility: visible;
    font-size: 12px;
}
