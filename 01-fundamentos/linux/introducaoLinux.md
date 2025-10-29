**title**: `Introdução ao Linux`

**date**: `2025-10-29`

**tags**: [`Introdução ao Linux`]

**difficulty**: `Avançado`

**status**: `Feito`

# **O que é um Kernel e GNU**

- ***Defina o kernel*** - O Linux que é um kernel não é um sistema operacional completo. Para o kernel ser um sistema completo precisa do `GNU`, 
que contém o `shell`, `utilitários`, `compilador`, `biblioteca` e `Ferramentas como editores de texto`.  Por essa razão, Richard M. Stallman, do projeto GNU, pede aos usuários que se refiram ao sistema completo como `GNU/Linux`. No apêndice, há mais informações sobre o projeto GNU. Pense no kernel como o motor de um carro. Ele é a parte essencial e central do sistema operacional, mas não é o carro inteiro.

- ***Função:*** Sua única função é gerenciar os recursos de hardware do computador.
- ***O que ele faz?*** Ele controla o processador (CPU), a memória (RAM), os dispositivos de entrada e saída (como teclado, mouse, discos rígidos) e permite que os programas (software) conversem com o hardware.
- ***Exemplo:*** O Linux é, tecnicamente, apenas um kernel. O NT Kernel é o kernel usado pelos sistemas Windows. O XNU é o kernel usado pela Apple no macOS e iOS.

- Um kernel sozinho não é muito útil para um usuário. Você não pode "abrir" um kernel ou "usar" um kernel. Ele é a fundação sobre a qual o resto do sistema é construído.

- ***O que é o GNU?*** Pense no GNU como todo o resto do carro: o chassi, o volante, os assentos, o painel e os pedais.
- ***Função:*** O GNU é um projeto que criou uma vasta coleção de software e ferramentas essenciais (chamados de userspace ou espaço do usuário) para formar um sistema operacional completo e livre, semelhante ao Unix.

- ***O que ele inclui:***
- ***A biblioteca C (glibc):*** A "caixa de ferramentas" fundamental que os programas usam para se comunicar com o kernel.
- ***O shell (Bash):*** A linha de comando que permite a você digitar comandos.
- ***Coreutils:*** Ferramentas básicas como ls (listar arquivos), cp (copiar), mv (mover).
- ***Compiladores (GCC):*** Ferramentas para criar novos programas.

# **Portabilidade**
 Linux é hoje um dos kernels de sistema operacional mais portados, rodando em sistemas desde o
 iPaq (`um computador portátil`) até o IBM S/390 (`um massivo e altamente custoso mainframe`), embora
 este tipo de portabilidade não fosse um dos objetivos principais de Linus Torvalds. Seu esforço era
 tornar seu sistema portátil no sentido de ter habilidade de facilmente compilar aplicativos de uma
 variedade de fontes no seu sistema. Portanto, o Linux originalmente se tornou popular em parte
 devido ao esforço para que as fontes GPL ou outras favoritas de todos rodassem no Linux.

**A prova mais clara disso está em seu famoso anúncio na Usenet (em agosto de 1991), onde ele disse:**
    "Estou fazendo um sistema operacional (gratuito) (apenas um hobby, não será grande e profissional como o gnu) para clones AT 386(486)."

    Todo o código inicial era "hardcoded" (escrito de forma fixa) para a arquitetura i386. Ele não tinha nenhuma intenção de fazê-lo rodar em qualquer outro tipo de processador, como SPARC, MIPS ou PowerPC.

    O objetivo inicial de Linus Torvalds não era a portabilidade. Seu objetivo era criar um kernel que funcionasse bem em seu computador 386. A portabilidade que vemos hoje (rodando em tudo, de supercomputadores a telefones) foi uma evolução que aconteceu depois, quando o projeto deixou de ser apenas um hobby pessoal e se tornou um esforço comunitário global.
    
# **Distribuiçoes**
 O sistema operacional completo (GNU/Linux) é considerado uma Distribuição Linux. É uma
 coleção de softwares livres (e às vezes não-livres) criados por indivíduos, grupos e organizações ao redor
 do mundo, e tendo o kernel como seu núcleo. Atualmente, companhias como a Red Hat, a SuSE,a
 MandrakeSoft ou a Conectiva, bem como projetos de comunidades com a Debian ou a Gentoo,
 compilam o software e fornecem um sistema completo, pronto para instalação e uso. Além disso, há
 projetos pessoais como o de Patrick Volkerding que fornece uma distribuição Linux, a Slackware e
 Carlos E. Morinoto que lançou a distribuição chamada Kurumin. Está última roda em CD, bastando
 as con gurações do computador aceitarem o boot pelo drive do CD.

 1. **O que Linus Torvalds Distribuía?**
- Linus distribuía apenas o código-fonte do kernel Linux.
- Versão 0.01 (Setembro de 1991): Não incluía quase nada além do código do kernel. Era basicamente apenas o código que fazia o hardware funcionar.
- Versão 0.02 (Outubro de 1991): Foi a primeira versão utilizável (embora muito limitada).
- O kernel por si só não tinha comandos visíveis, apenas as chamadas internas para a CPU e o hardware.

2. **Os Primeiros Comandos (do "Sistema")**
- O primeiro "sistema operacional" funcional era composto pelo kernel Linux + um punhado de ferramentas cruciais de um outro sistema, o Minix (o sistema operacional que Linus estava usando na época para desenvolver o Linux).
- Os comandos que os usuários tinham acesso eram os comandos básicos do Minix, que precisavam ser copiados manualmente para dentro do novo ambiente Linux.
- No entanto, o objetivo final e o que se popularizou foi o uso das ferramentas do Projeto GNU.
- **O "Shell" (Interpretador de Comandos):** Inicialmente, os usuários precisavam de um shell para interagir com o kernel. O mais comum era o Bash (Bourne-Again Shell), que fazia parte do projeto GNU.

- **Os Comandos Básicos (Coreutils): Os primeiros usuários precisavam de ferramentas como:**

- ls (listar arquivos)
- cp (copiar)
- mv (mover)
- rm (deletar)
- cat (concatenar e exibir conteúdo de arquivos)

- **Esses comandos, essenciais para interagir com o sistema de arquivos que o kernel gerenciava, vinham do Projeto GNU (ou inicialmente do Minix).**

3. **Os Programas que os Usuários Tinham que Configurar**
- O usuário que quisesse ter um sistema funcional, um verdadeiro GNU/Linux, tinha que arranjar, compilar e configurar todo o userspace (o espaço do usuário) por conta própria.

- **Os principais programas que os usuários tinham que obter eram:**
``` bash copy
______________________________________________________________________________________
|   Categoria  	  |  Programas/Ferramentas	|                  Uso                    |
|_________________|_________________________|_________________________________________|
|    Básico	      | GNU C Library (glibc)	|  A biblioteca fundamental que quase     |
|                 |                         |  todos os programas (incluindo o shell  |
|                 |                         |  e as coreutils) usam para se comunicar |
|                 |                         |  com o kernel. Sem ela, nada rodava.    |
|_________________|_________________________|_________________________________________|                
|  Shell/Linha    |         Bash            |  O interpretador de comandos principal  |
|  de Comando	  |                         |  do GNU                                 |
|_________________|_________________________|_________________________________________|                                               
|    Utilitários  |    Coreutils do GNU     |  O conjunto de comandos básicos         |
|    Essenciais	  |	                        |  (ls, cp, mv, etc.).                    |
|_________________|_________________________|_________________________________________|
| Desenvolvimento |           GCC           |                                         |
|                 |                         |  O compilador C. Crucial porque a       |
|                 |                         |  maioria das ferramentas e do kernel    |
|                 |                         |  precisava ser compilada a partir do    |
|                 |                         |  código-fonte.                          | 
|_________________|_________________________|_________________________________________|
| Edição de Texto	    GNU Emacs / Vi	    |  Editores de texto para escrever código |
|                                           |  ou configurar arquivos.                |                                                           
|___________________________________________|_________________________________________|
```
Basicamente, o esforço inicial era tremendo: você pegava o kernel de Linus e as ferramentas do GNU (todas em código-fonte), compilava o kernel, depois compilava o glibc, e só então você conseguia compilar todas as outras ferramentas do GNU para ter um ambiente onde você pudesse, finalmente, rodar outros programas.

Foi exatamente para simplificar esse processo que surgiram as primeiras Distribuições Linux (como o MCC Interim Linux e, logo depois, o SLS e o Debian), que faziam esse trabalho de juntar o kernel e as ferramentas GNU para o usuário.

# Temas estudados
- <p style="color: dodgerblue;">Introdução ao linux</p>
- <p style="color: dodgerblue;">A diferança entre o kernel e o GNU</p>
- <p style="color: dodgerblue;">A função do kernel e o que o kernel faz</p>
- <p style="color: dodgerblue;">Funções essenciais do GNU</p>
- <p style="color: dodgerblue;">O objetivo de linus não era a Portabilidade</p>
- <p style="color: dodgerblue;">Distribuição Linux</p>


# Exercício

***Se você conseguir responder as perguntas sobre a introdução ao linux, então você possui um conhecimento sólido ao linux.*** 

1. **Defina kernel?**

2. **Defina GNU?**

3. **Explique por que precisam estar juntos o Kernel e GNU?**

4. **Quem criou Linux e onde foi?**

5. **Sobre o Minix e o padrão POSIX**

6. **Data do lançamento GNU/Linux?**

7. **Porque linus criou o linux?**

8. **Comunidade começou a colaborar**

9. **Portabilidade se tornou um dos pontos fortes quando?**

10. **O que é uma distribuição Linux?**

11. **A primeira distribuição MCC?**

12. **Por que existem várias?**