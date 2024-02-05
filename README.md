# html3
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF=8">
        <Title>Регистр</Title>
        <style>
* {
  box-sizing: border-box;
}
body {
  align-items: center;
  background-color: #000;
  display: flex;
  justify-content: center;
  height: 100vh;
  font-family: sans-serif;
}

.form {
  background-color: #15172b;
  border-radius: 20px;
  min-height: 500px;
  padding: 20px;
  width: 320px;
}

.title {
  color: #eee;
  font-size: 36px;
  font-weight: 600;
  margin-top: 30px;
}

.subtitle {
  color: #eee;
  font-size: 16px;
  font-weight: 600;
  margin-top: 10px;
}

.input-container {
  height: 50px;
  position: relative;
  width: 100%;
}

.ic1 {
  margin-top: 40px;
}

.ic2 {
  margin-top: 30px;
}

.input {
  background-color: #303245;
  border-radius: 12px;
  border: 0;
  color: #eee;
  font-size: 18px;
  height: 100%;
  outline: 0;
  padding: 4px 20px 0;
  width: 100%;
}

.cut {
  background-color: #15172b;
  border-radius: 10px;
  height: 20px;
  left: 20px;
  position: absolute;
  top: -20px;
  transform: translateY(0);
  transition: transform 200ms;
  width: 76px;
}

.cut-short {
  width: 50px;
}

.input:focus ~ .cut,
.input:not(:placeholder-shown) ~ .cut {
  transform: translateY(8px);
}

.placeholder {
  color: #65657b;
  left: 20px;
  line-height: 14px;
  pointer-events: none;
  position: absolute;
  transform-origin: 0 50%;
  transition: transform 200ms, color 200ms;
  top: 20px;
}

.input:focus ~ .placeholder,
.input:not(:placeholder-shown) ~ .placeholder {
  transform: translateY(-30px) translateX(10px) scale(0.75);
}

.input:not(:placeholder-shown) ~ .placeholder {
  color: #808097;
}

.input:focus ~ .placeholder {
  color: #dc2f55;
}

.submit {
  background-color: #08d;
  border-radius: 12px;
  border: 0;
  color: #eee;
  cursor: pointer;
  font-size: 18px;
  height: 50px;
  margin-top: 38px;
  text-align: center;
  width: 100%;
}

.submit:active {
  background-color: #06b;
}

p {
  margin-bottom: 0;
}
a, a:link, a:hover, a:visited {
  color: #808097;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
        </style>
    </head>
    <body>
        <div class="form">
            <div class="title"></div>
            <div class="subtitle">Регистрация</div>
            <div class="input-container ic1">
              <input id="firstname" class="input" type="text" placeholder=" " />
              <div class="cut"></div>
              <label for="firstname" class="placeholder">Имя</label>
            </div>
            <div class="input-container ic2">
              <input id="lastname" class="input" type="text" placeholder=" " />
              <div class="cut"></div>
              <label for="lastname" class="placeholder">Фамилия</label>
            </div>
            <div class="input-container ic2">
              <input id="email" class="input" type="text" placeholder=" " />
              <div class="cut cut-short"></div>
              <label for="email" class="placeholder">Город<label>
            </div>
            <div class="input-container ic2">
                <input id="email" class="input" type="text" placeholder=" " />
                <div class="cut cut-short"></div>
                <label for="email" class="placeholder">Пароль<label>
              </div>
            <button type="text" class="submit">Подтвердить</button>
          </div>
    </body>
</html>
