# X-Men com tema de Cavaleiros do Zodíaco

Uma seleção interativa de personagens inspirada na estética dos menus de jogos dos X-Men dos anos 90 e no universo de **Os Cavaleiros do Zodíaco**. O projeto foi desenvolvido como exercício de front-end e combina uma interface nostálgica com uma navegação simples e responsiva.

> Projeto demonstrativo para fins de estudo. X-Men e Os Cavaleiros do Zodíaco são marcas de seus respectivos detentores.

## Demonstração

![Prévia da seleção de personagens](https://github.com/lfbond/projeto_xmen_tema-cavaleirosZodiaco/assets/69223872/82748559-a6b3-4578-aed9-6eb37eaeb52c)

A versão publicada pode ser acessada pelo [GitHub Pages](https://lfbond.github.io/projeto_xmen_tema-cavaleirosZodiaco/).

## Recursos

- Seleção inicial com Atena em destaque.
- Lista com 20 personagens e suas respectivas imagens em formato de card.
- Atualização instantânea da imagem ampliada, do nome e da descrição ao passar o cursor sobre um personagem.
- Destaque visual do personagem ativo com borda e sombra inspiradas no cosmo.
- Rolagem na lista de personagens para acomodar todo o elenco.
- Layout adaptado para desktops, tablets e celulares.
- No celular, ao selecionar um personagem, a página volta suavemente para a área de detalhes.

## Personagens disponíveis

### Bronze

Atena, Seiya de Pegasus, Shiryu de Dragão, Hyoga de Cisne, Shun de Andrômeda e Ikki de Fênix.

### Ouro

Mu de Áries, Shion de Áries, Aldebaran de Touro, Saga de Gêmeos, Kanon de Gêmeos, Máscara da Morte de Câncer, Aiolia de Leão, Shaka de Virgem, Dohko de Libra, Milo de Escorpião, Aiolos de Sagitário, Shura de Capricórnio, Camus de Aquário e Afrodite de Peixes.

## Tecnologias

- **HTML5** para a estrutura semântica da página.
- **CSS3** para layout, identidade visual, fundo, tipografia e estados de seleção.
- **JavaScript puro** para os eventos de seleção e atualização dos dados do personagem.
- **Google Fonts**, com a família Oxanium usada na interface.
- **GitHub Pages** para publicação.

## Estrutura do projeto

```text
.
├── index.html              # Página principal e dados dos personagens
├── README.md
└── src/
    ├── assets/              # Logo, fundo, cards e imagens ampliadas
    ├── css/
    │   ├── reset.css        # Reset básico dos estilos
    │   ├── estilos.css      # Estilos principais da interface
    │   └── responsivo.css   # Regras para telas menores
    └── js/
        └── index.js         # Lógica de seleção e atualização do detalhe
```

## Como executar localmente

O projeto não possui dependências ou etapa de compilação. É necessário apenas um navegador.

### Opção 1: abrir diretamente

1. Clone o repositório:

   ```bash
   git clone https://github.com/lfbond/projeto_xmen_tema-cavaleirosZodiaco.git
   ```

2. Entre na pasta do projeto:

   ```bash
   cd projeto_xmen_tema-cavaleirosZodiaco
   ```

3. Abra o arquivo `index.html` no navegador.

### Opção 2: usar um servidor local

Servir a pasta localmente é útil para testar o projeto em diferentes dispositivos. Com o Python instalado, execute:

```bash
python -m http.server 8000
```

Depois, acesse <http://localhost:8000> no navegador.

## Como funciona

Cada item da lista possui um `id`, um `data-name` e um `data-description` no `index.html`. O arquivo `src/js/index.js` escuta o evento `mouseenter`, remove a seleção anterior e usa esses dados para atualizar o painel principal. A imagem ampliada é localizada automaticamente em `src/assets/` a partir do `id` do personagem.

Para adicionar um novo personagem:

1. Inclua uma imagem de card seguindo o padrão `card-nome-do-personagem-min.png`.
2. Inclua a imagem ampliada com o mesmo identificador usado no `id`, por exemplo `nome-do-personagem.png`.
3. Adicione um novo item `<li class="personagem">` em `index.html` com `id`, `data-name`, `data-description` e a imagem do card.

## Melhorias planejadas

- Adicionar suporte completo à seleção por teclado e a outros recursos de acessibilidade.
- Incluir efeitos sonoros opcionais nas interações.
- Criar uma forma de alternar entre diferentes temas visuais.
- Ampliar o elenco com novos personagens e descrições revisadas.

## Contribuição

Sugestões e correções são bem-vindas. Para contribuir, abra uma issue descrevendo a proposta ou envie um pull request com uma alteração pequena e documentada.

## Licença

Este repositório não contém atualmente um arquivo `LICENSE`. O código e os assets devem ser tratados como material de estudo, respeitando os direitos autorais e as marcas dos personagens representados.

