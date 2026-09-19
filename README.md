# Automação de usuários e permissões no Linux

Projeto desenvolvido para praticar administração de sistemas Linux e automação com Shell Script.

O script cria uma estrutura de diretórios, grupos e usuários, configurando proprietários e permissões de acesso de acordo com cada setor.

## Objetivo

Automatizar tarefas administrativas que normalmente seriam executadas manualmente, garantindo uma configuração padronizada e reduzindo erros durante a criação de usuários e permissões.

## Funcionalidades

O script realiza as seguintes tarefas:

- Criação dos diretórios `/publico`, `/adm`, `/ven` e `/sec`
- Criação dos grupos `GRP_ADM`, `GRP_VEN` e `GRP_SEC`
- Criação de usuários para cada grupo
- Definição do Bash como shell padrão dos usuários
- Configuração dos proprietários dos diretórios
- Aplicação de permissões específicas para cada setor
- Liberação do diretório público para todos os usuários

## Estrutura criada

| Diretório | Grupo responsável | Permissão | Finalidade |
|---|---|---:|---|
| `/adm` | `GRP_ADM` | `770` | Área administrativa |
| `/ven` | `GRP_VEN` | `770` | Área de vendas |
| `/sec` | `GRP_SEC` | `770` | Área de secretaria |
| `/publico` | Todos os usuários | `777` | Área compartilhada |

## Distribuição dos usuários

| Grupo | Usuários |
|---|---|
| `GRP_ADM` | carlos, joao e maria |
| `GRP_VEN` | debora, sebastiana e roberto |
| `GRP_SEC` | josefina, amanda e rogerio |

## Tecnologias utilizadas

- Linux
- Shell Script
- Bash
- Gerenciamento de usuários e grupos
- Permissões de arquivos e diretórios
- Git e GitHub

## Como executar

Clone o repositório:

```bash
git clone https://github.com/FDavidPereira/linux-projeto1.git
```

Entre no diretório:

```bash
cd linux-projeto1
```

Conceda permissão de execução:

```bash
chmod +x projeto01.sh
```

Execute o script com privilégios administrativos:

```bash
sudo ./projeto01.sh
```

## Verificação

Depois da execução, os grupos podem ser verificados com:

```bash
getent group GRP_ADM
getent group GRP_VEN
getent group GRP_SEC
```

As permissões dos diretórios podem ser verificadas com:

```bash
ls -ld /publico /adm /ven /sec
```

## Observações de segurança

Este projeto foi criado para fins educacionais e deve ser executado somente em uma máquina virtual ou ambiente de laboratório.

A versão inicial utiliza uma senha padrão para demonstrar a criação automatizada de usuários. Em um ambiente real, senhas não devem ficar armazenadas diretamente no código.

O diretório `/publico` utiliza a permissão `777` para atender ao exercício proposto. Em ambientes reais, devem ser aplicadas permissões mais restritivas, seguindo o princípio do menor privilégio.

## Aprendizados

Com este projeto, pratiquei:

- Automação de tarefas administrativas
- Criação e gerenciamento de usuários
- Organização de usuários em grupos
- Controle de acesso a diretórios
- Permissões numéricas no Linux
- Execução de scripts com privilégios administrativos
- Documentação técnica de projetos

## Autor

**David de Assis Pereira**

[LinkedIn](https://www.linkedin.com/in/f-david-pereira/) | [GitHub](https://github.com/FDavidPereira)
