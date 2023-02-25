# Ldap_MVC_Spring
"Ldap_MVC_Spring é um pacote que integra o Spring Boot com LDAP, permitindo o gerenciamento completo de usuários em servidores LDAP de forma simples e eficiente. Spring Boot >=2.2.0, Java >=11


Com esse pacote, é possível realizar operações de adição, exclusão, atualização e filtro de usuários no servidor LDAP de maneira organizada e intuitiva, utilizando uma arquitetura MVC (Model-View-Controller) robusta e escalável. O Ldap_MVC_Spring é um projeto de código aberto, disponível no GitHub, e pode ser facilmente integrado a outros projetos de software. Confira agora mesmo e simplifique o gerenciamento de usuários em servidores LDAP!"

Na classe LdapService:

[authenticate(userDn: String, password: String)]: Método que realiza a autenticação de um usuário no servidor LDAP, recebendo o DN do usuário e sua senha como parâmetros. Retorna true se a autenticação for bem-sucedida, e false caso contrário.

[createUser(user: LdapUser)]: Método que cria um novo usuário no servidor LDAP, recebendo um objeto do tipo LdapUser como parâmetro. Esse objeto deve conter os campos cn, givenName, sn, userPrincipalName e unicodePwd preenchidos com os valores correspondentes.

[modifyUser(user: LdapUser)]: Método que atualiza os dados de um usuário existente no servidor LDAP, recebendo um objeto do tipo LdapUser como parâmetro. Esse objeto deve conter o campo cn preenchido com o valor correspondente ao usuário que se deseja atualizar, e os demais campos com os novos valores.

[deleteUser(cn: String)]: Método que exclui um usuário existente no servidor LDAP, recebendo como parâmetro o valor do campo cn correspondente ao usuário que se deseja excluir.

[addUserToGroup(cnUser: String, cnGroup: String)]: Método que adiciona um usuário existente no servidor LDAP a um grupo também existente, recebendo como parâmetros os valores dos campos cn correspondentes ao usuário e ao grupo.

[removeUserFromGroup(cnUser: String, cnGroup: String)]: Método que remove um usuário existente no servidor LDAP de um grupo também existente, recebendo como parâmetros os valores dos campos cn correspondentes ao usuário e ao grupo.

[getAllUsers()]: Método que retorna uma lista de objetos LdapUser contendo todos os usuários cadastrados no servidor LDAP.

Na classe LdapUser:

[cn: String]: Nome comum do usuário.
[givenName: String]: Nome próprio do usuário.
[sn: String]: Sobrenome do usuário.
[userPrincipalName: String]: Nome principal do usuário, que geralmente é o seu endereço de email.
[unicodePwd: String]: Senha do usuário, codificada em UTF-8.
