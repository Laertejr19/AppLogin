# 🔐 App Login

Aplicativo Android simples desenvolvido em **Java + XML** no **Android Studio**, que permite ao usuário realizar login utilizando um nome de usuário e senha.  
Projeto criado como parte dos estudos de **desenvolvimento mobile nativo** e para praticar autenticação básica no Android.

---

## 🧠 Sobre o Projeto

O **App Login** oferece uma interface onde o usuário pode inserir seu nome de usuário e senha. Ao clicar no botão de login, o aplicativo verifica se as credenciais correspondem a um conjunto pré-definido e, em caso afirmativo, permite o acesso à próxima tela.  
O objetivo é demonstrar como implementar um sistema de login simples em um aplicativo Android.

---

## 🛠️ Tecnologias Utilizadas

| Categoria         | Ferramenta                         |
|-------------------|------------------------------------|
| IDE               | Android Studio                     |
| Linguagem         | Java                               |
| Layouts           | XML                                |
| Versão mínima Android | API 21 (Android 5.0)             |
| Estrutura de UI   | ConstraintLayout / LinearLayout    |

---

## 📱 Estrutura do Projeto

```
app/
 ├── java/
 │    └── br/ulbra/appLogin/
 │         └── MainActivity.java
 ├── res/
 │    ├── layout/
 │    │     └── activity_main.xml
 │    ├── drawable/
 │    │     └── (ícones ou imagens do app)
 │    └── values/
 │          └── strings.xml
 └── AndroidManifest.xml
```

---

## 🔑 Lógica de Login

```java
EditText edtUsuario = findViewById(R.id.edtUsuario);
EditText edtSenha = findViewById(R.id.edtSenha);
Button btnLogin = findViewById(R.id.btnLogin);

btnLogin.setOnClickListener(v -> {
    String usuario = edtUsuario.getText().toString();
    String senha = edtSenha.getText().toString();
    if (usuario.equals("admin") && senha.equals("1234")) {
        // Acesso permitido
        Intent intent = new Intent(MainActivity.this, TelaPrincipal.class);
        startActivity(intent);
    } else {
        // Acesso negado
        Toast.makeText(MainActivity.this, "Credenciais inválidas", Toast.LENGTH_SHORT).show();
    }
});
```

---

## 🏗️ Funcionalidades Implementadas

✅ Tela de login com campos para usuário e senha  
✅ Validação simples de credenciais  
✅ Navegação para a tela principal após login bem-sucedido  
✅ Interface simples e funcional  
✅ Código comentado para entendimento  

---

## 💡 Possíveis Melhorias

- Implementar autenticação com banco de dados ou API externa  
- Adicionar funcionalidade de "esqueci minha senha"  
- Implementar autenticação com biometria (impressão digital ou reconhecimento facial)  
- Criar tela de cadastro de novos usuários  
- Adicionar animações e transições entre telas  

---

## 👩‍💻 Autor

**Nome:** *Laerte Ferraz da Silva Júnior*  
**Instituição:** *Curso Técnico em Informática – Escola Ulbra São Lucas*  
**Disciplina:** *Desenvolvimento Mobile Android*  
**Professor:** *Jeferson Leon*  

---

## 📚 Licença

Projeto desenvolvido para fins **educacionais**.  
Livre para uso e modificação, desde que mantidos os créditos ao autor.

---

> “A melhor forma de aprender é construindo. Então... bora codar!”
