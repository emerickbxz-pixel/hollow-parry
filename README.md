# Hollow Parry

Protótipo de jogo 2D no estilo Hollow Knight, feito só com HTML, CSS e JavaScript.

O protagonista é um monge-guerreiro **sem armas**. Ele tem só um escudo, e a
única forma de atacar é **aparar** os golpes dos inimigos.

## Como rodar

1. Baixe ou clone este repositório.
2. Abra o arquivo `index.html` no navegador (Chrome, Edge, Firefox...).

Para testar no celular pela mesma rede Wi-Fi, use um servidor local simples
dentro da pasta do projeto:

```bash
python3 -m http.server 8000
```

Depois, no celular, acesse `http://IP-DO-COMPUTADOR:8000`.

## Como jogar

- **Celular:** use os botões embaixo da tela (◀ ▶ Pular Aparar).
- **Computador:** setas ou A/D andam, Espaço ou W pula, J ou Z apara.

## Regra da aparada

1. Quando um inimigo vai bater, aparece um **anel branco** em volta dele e um **"!"** sobre a cabeça.
2. O anel encolhe até o golpe.
3. Aperte **Aparar** quando o anel ficar **verde**. Essa é a janela da aparada perfeita.
4. A aparada devolve o golpe para o inimigo.
5. Cada aparada perfeita **seguida** dobra o dano devolvido: x1, x2, x4, x8... (o máximo é x16).
6. Se você levar um golpe, ou apertar Aparar fora da hora, a sequência volta para zero.

## Arquivos

- `index.html`: o jogo inteiro. O CSS (layout e cores) e o JavaScript (toda a lógica) ficam dentro dele, então basta esse arquivo para abrir o jogo.

## Como ajustar o jogo

As configurações ficam no `index.html`, dentro da tag `<script>`, na parte "Configurações".
Por exemplo, para o inimigo bater mais devagar, aumente o `tempoPreparo` dele.
Para deixar a aparada mais fácil, aumente `JANELA_APARAR`.
