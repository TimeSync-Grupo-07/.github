# 📘 Utilização dos Repositórios

Este documento foi criado para **auxiliar e explicitar** a forma de utilização das regras de **commits** e **branches** em todos os repositórios que estão ou serão criados nesta organização.  
O objetivo é **facilitar a rastreabilidade** e **aumentar os níveis de segurança** no momento do *deploy* da solução.

---

## 🌿 Branches

### 🔧 Dev
- Área de desenvolvimento da parte técnica do projeto.
- Após finalização, o código será enviado para a branch `Homolog`.

#### 🔐 Permissões:
- ✅ Todos têm acesso a essa branch.
- ❌ Sem proteção contra commits diretos.

---

### 🧪 Homolog
- Ambiente de testes de funcionamento do código em toda a infraestrutura.
- Qualquer solução, independente da linguagem, será validada quanto a comportamentos inesperados ou bugs.

#### 🔐 Permissões:
- ✅ *Commits* apenas via **Pull Request**.
- ✅ *Pull Request* será aprovado mediante testes automatizados.

---

### 🚀 main
- Branch onde estão os códigos prontos para produção.

#### 🔐 Permissões:
- ✅ Apenas **Davi R. da Silva** pode realizar commits.
- ❌ Demais membros da organização não terão permissão de escrita.

---

## ✍️ Commits

Os *commits* devem seguir o seguinte padrão de escrita:

1. **Tipo da ação**  
   Ex: `Criação`, `Correção`, `Teste`

2. **Funcionalidade/parte alterada**  
   Ex: `Criação - Nova funcionalidade de Login por SSO`

3. **Estado do código**  
   Ex: `Finalizado`, `Em desenvolvimento`, `Em teste`  
   Exemplo completo:  
   `Criação - Nova funcionalidade de Login por SSO - Finalizado`

---

## 🧭 Exemplo de Uso

### 🔄 Atualize o repositório e acesse a branch `Dev`:
```bash
git pull
git checkout Dev
```
### 🛠️ Após realizar suas modificações, execute:
```bash
git add .
git commit -m "Criação - Nova funcionalidade de Login por SSO - Teste"
git push
```