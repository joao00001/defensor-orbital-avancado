# Defensor Orbital Avançado

## Descrição Breve

**Defensor Orbital Avançado** é um jogo de arcade 2D desenvolvido em HTML5, CSS3 e JavaScript puro. O jogador controla um escudo orbital com o objetivo de proteger um planeta central contra ondas crescentes de inimigos e seus projéteis. O jogo apresenta diferentes tipos de inimigos, power-ups e um sistema de pontuação e progressão por ondas.

## Tecnologias Utilizadas

* **HTML5**: Estrutura base da página e elemento `<canvas>` para renderização do jogo.
* **CSS3**: Estilização da interface do usuário (HUD, menus de início/fim de jogo/pausa) e animações básicas.
* **JavaScript (ES6+)**:
    * Lógica completa do jogo (movimentação, colisões, IA dos inimigos, power-ups, sistema de ondas).
    * Renderização gráfica 2D utilizando a Canvas API.
    * Manipulação do DOM para a interface do usuário e feedback.
    * Programação Orientada a Objetos para representar entidades do jogo (Planeta, Defensor, Inimigos, Projéteis, Partículas, Power-ups).

## Como Executar

1.  **Clone o repositório ou baixe os arquivos.**
    ```bash
    git clone [https://github.com/joao00001/defensor-orbital-avancado.git](https://github.com/joao00001/defensor-orbital-avancado.git)
    cd defensor-orbital-avancado
    ```
2.  **Configure os Assets (Recursos Gráficos):**
    * O jogo utiliza sprites para os elementos visuais (planeta, defensor, inimigos, etc.).
    * No arquivo `index.html`, localize o objeto `assetSources` dentro da tag `<script>`.
    * Substitua os caminhos placeholder (ex: `'path/to/your/planet-sprite.png'`) pelos caminhos corretos dos seus arquivos de imagem.
    * Se nenhum asset for fornecido, o jogo utilizará formas geométricas básicas como fallback.
3.  **Abra o Arquivo `index.html`:**
    * Navegue até o diretório onde o arquivo `index.html` está localizado.
    * Abra `index.html` em qualquer navegador web moderno que suporte HTML5 Canvas (Google Chrome, Firefox, Edge, Safari).

## Controles do Jogo

* **Mouse**: Mova o cursor do mouse ao redor do planeta central para rotacionar o escudo orbital.
* **Touch (Dispositivos Móveis)**: Deslize o dedo na tela ao redor do planeta central para rotacionar o escudo.

## Estrutura do Código

O projeto consiste em um único arquivo `index.html` que contém:
* **HTML**: A estrutura básica da página, incluindo o elemento `canvas` e os contêineres para a UI (tela de início, game over, pausa, placar).
* **CSS**: Embutido na tag `<style>`, responsável pela aparência visual de todos os elementos da interface do usuário e animações (como o efeito "shake").
* **JavaScript**: Embutido na tag `<script>`, contém toda a lógica do jogo, incluindo:
    * **Gerenciamento de Assets**: Carregamento de imagens.
    * **Classes de Entidades**: `Planet`, `Defender`, `Enemy`, `Projectile`, `PowerUp`, `Particle` para modelar os objetos do jogo.
    * **Lógica de Jogo**: Loop principal (`gameLoop`), atualizações de estado (`updateGame`), renderização (`drawGame`), detecção de colisão (`checkCollisions`), sistema de ondas (`spawnWave`), gerenciamento de power-ups, pontuação e vidas.
    * **Manipulação da UI**: Funções para exibir/ocultar telas, atualizar placar, etc.
    * **Controles**: Event listeners para mouse e touch.
    * **Efeitos Visuais**: Sistema de partículas para explosões, impactos, etc., e fundo com paralaxe e estrelas dinâmicas.

## Considerações Técnicas

* **Responsividade**: A interface do usuário (menus e HUD) foi ajustada com CSS para oferecer uma melhor experiência em telas menores (dispositivos móveis).
* **Performance**: O jogo utiliza `requestAnimationFrame` para o loop principal, visando animações fluidas. O `deltaTime` é calculado para normalizar a velocidade do jogo em diferentes taxas de atualização.
* **Sem Dependências Externas**: O jogo é construído inteiramente com tecnologias web padrão (HTML, CSS, JS) e não requer bibliotecas ou frameworks externos para funcionar (além dos assets gráficos que você fornecerá).

---

Este README fornece uma visão geral técnica do projeto "Defensor Orbital Avançado".
