# Portswigger-Labs PT-BR

## 🔐 Vulnerabilidades de Autenticação

Conceitualmente, as vulnerabilidades de autenticação são fáceis de entender. No entanto, elas costumam ser críticas devido à relação direta entre autenticação e segurança.  

As vulnerabilidades de autenticação podem permitir que invasores obtenham acesso a dados e funcionalidades sensíveis. Além disso, elas expõem uma superfície de ataque adicional para novas explorações. Por esse motivo, é importante aprender a identificar e explorar vulnerabilidades de autenticação, além de saber como contornar medidas de proteção comuns.  

### 📌 Nesta seção, explicamos:
- Os mecanismos de autenticação mais comuns usados por sites.
- As possíveis vulnerabilidades nesses mecanismos.
- Vulnerabilidades inerentes a diferentes tipos de autenticação.
- Vulnerabilidades típicas introduzidas por uma implementação inadequada.
- Como tornar seus próprios mecanismos de autenticação o mais robustos possível.

![Autenticação Vulnerável](https://portswigger.net/web-security/images/password-reset-poisoning.svg)

---

## 🛠 Laboratórios  

Se você já está familiarizado com os conceitos básicos sobre vulnerabilidades de autenticação e deseja praticar a exploração dessas falhas em alvos realistas e propositalmente vulneráveis, você pode acessar os laboratórios sobre esse tópico no link abaixo.  

🔗 **[Veja todos os laboratórios de autenticação](https://portswigger.net/web-security/all-labs#authentication)**  

---

## ❓ O que é autenticação?  

Autenticação é o processo de verificar a identidade de um usuário ou cliente. Como os sites estão potencialmente expostos a qualquer pessoa conectada à internet, mecanismos de autenticação robustos são essenciais para garantir a segurança na web.  

### 🔑 Três principais tipos de autenticação:
1. **Algo que você sabe** – Como uma senha ou a resposta a uma pergunta de segurança. Esses fatores são chamados de *"fatores de conhecimento"*.
2. **Algo que você tem** – Um objeto físico, como um telefone celular ou um token de segurança. Esses fatores são chamados de *"fatores de posse"*.
3. **Algo que você é ou faz** – Como biometria (impressão digital, reconhecimento facial) ou padrões de comportamento. Esses fatores são chamados de *"fatores de inerência"*.  

Os mecanismos de autenticação utilizam diferentes tecnologias para verificar um ou mais desses fatores.  

---

## 🔄 Qual a diferença entre autenticação e autorização?  

- **Autenticação** verifica se o usuário é realmente quem afirma ser.  
- **Autorização** verifica se um usuário tem permissão para realizar uma ação específica.  

Por exemplo, quando um usuário tenta acessar um site com o nome de usuário `Carlos123`, a autenticação determina se ele realmente é o dono dessa conta.  

Depois que `Carlos123` é autenticado, suas permissões definem o que ele está autorizado a fazer. Ele pode, por exemplo, ter permissão para visualizar informações pessoais de outros usuários ou realizar ações como excluir uma conta.  

---

## ⚠ Como surgem as vulnerabilidades de autenticação?  

A maioria das vulnerabilidades nos mecanismos de autenticação ocorre de duas formas principais:  

1. **Mecanismos fracos de autenticação** – Não oferecem proteção adequada contra ataques de força bruta.  
2. **Falhas de lógica ou implementação** – Erros na codificação permitem que invasores contornem completamente a autenticação. Isso é chamado de *"autenticação quebrada"* (**broken authentication**).  

Em muitas áreas do desenvolvimento web, falhas lógicas podem fazer um site se comportar de maneira inesperada. Isso pode ou não representar um problema de segurança. No entanto, devido à importância da autenticação para a segurança, qualquer falha na lógica da autenticação tem alta probabilidade de expor o site a riscos graves.  

---

## 🚨 Qual o impacto de uma autenticação vulnerável?  

As vulnerabilidades de autenticação podem ter consequências severas. Se um invasor conseguir contornar a autenticação ou realizar um ataque de força bruta para acessar a conta de outro usuário, ele terá acesso a todos os dados e funcionalidades dessa conta.  

Se a conta comprometida for de um **administrador do sistema**, o invasor pode obter controle total sobre toda a aplicação e até mesmo acessar a infraestrutura interna.  

Mesmo a invasão de uma conta de **baixo privilégio** pode ser perigosa, pois pode conceder acesso a informações comerciais sensíveis ou permitir que o invasor acesse páginas internas que aumentam a superfície de ataque. Muitos ataques graves não são possíveis a partir de páginas públicas, mas podem ser explorados a partir de páginas internas.  

---

## 🔍 Vulnerabilidades em mecanismos de autenticação  

O sistema de autenticação de um site geralmente é composto por vários mecanismos distintos, onde vulnerabilidades podem ocorrer. Algumas falhas são comuns em diferentes contextos, enquanto outras são específicas para determinados tipos de autenticação.  

A seguir, analisamos as vulnerabilidades mais comuns em três áreas:  

🔗 [Vulnerabilidades em login baseado em senha](https://portswigger.net/web-security/authentication/password-based)  
🔗 [Vulnerabilidades em autenticação multifator](https://portswigger.net/web-security/authentication/multi-factor)  
🔗 [Vulnerabilidades em outros mecanismos de autenticação](https://portswigger.net/web-security/authentication/other-mechanisms)  

Muitos dos laboratórios disponíveis requerem a enumeração de nomes de usuário e ataques de força bruta contra senhas. Para auxiliar nesse processo, é fornecida uma lista com candidatos de nomes de usuário e senhas que podem ser usados para resolver os desafios.  

---

## 🔗 Vulnerabilidades em autenticação de terceiros  

Se você gosta de explorar falhas em mecanismos de autenticação e já completou os desafios principais, pode tentar os **laboratórios sobre autenticação OAuth**.  

🔗 [OAuth authentication](https://portswigger.net/web-security/oauth)  

---

## 🛡️ Prevenção de ataques nos seus próprios mecanismos de autenticação  

Já demonstramos diversas maneiras pelas quais os sites podem ser vulneráveis devido à forma como implementam a autenticação.  

Para reduzir o risco de ataques nos seus próprios sites, é essencial seguir alguns princípios fundamentais. A seguir, apresentamos algumas boas práticas para fortalecer a segurança dos mecanismos de autenticação e minimizar vulnerabilidades.  

🔗 [Como proteger seus mecanismos de autenticação](https://portswigger.net/web-security/authentication/securing)  
