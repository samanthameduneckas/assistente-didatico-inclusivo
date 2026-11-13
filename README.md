# Assistente Didático Inclusivo

Aplicação web que usa **IA generativa (Google Gemini)** para adaptar textos didáticos a alunos com **TEA** e **TDAH**. Nasceu da minha experiência na educação pública e especial e da minha formação em Engenharia de Software.

Desenvolvido com apoio do Google Gemini. Revisei, testei e ajustei o código e os prompts.

## Como funciona

1. A pessoa cola sua chave da API Gemini (gratuita no Google AI Studio).
2. Cola o texto da aula e escolhe a necessidade (TEA ou TDAH).
3. O JavaScript envia o texto e um **prompt específico** à API Gemini (`fetch` assíncrono) e mostra a resposta na tela.

### Os prompts

Cada necessidade tem instruções próprias (`PROMPTS` no `index.html`):

- **TEA:** linguagem literal e direta, blocos curtos com títulos claros, ordem cronológica, pergunta simples de compreensão.
- **TDAH:** parágrafos curtos, passos numerados ou meta clara, pergunta de atenção.

## Segurança e privacidade

- A chave **não fica no código nem no repositório**: é digitada pelo usuário e guardada apenas na sessão da aba (`sessionStorage`).
- O texto é enviado à API do Google. **Não use nomes reais ou dados pessoais de alunos.**
- Revise sempre o material gerado antes de usar com os alunos: a IA pode errar.

## Tecnologias

HTML5, CSS3, JavaScript (fetch/async-await) e API Gemini.

## Como usar

1. Gere uma chave em [Google AI Studio](https://aistudio.google.com/).
2. Abra o `index.html` no navegador (ou pelo GitHub Pages).
3. Cole a chave, o texto e clique em **Gerar material adaptado**.

Se aparecer erro de modelo não encontrado, atualize a constante `MODELO` no início do script com o nome atual do modelo.

## Próximos passos

- [ ] Mais opções de adaptação (por exemplo, simplificação de linguagem)
- [ ] Botão para copiar o resultado
- [ ] Exemplos de "antes e depois" no README
- [ ] Backend simples para não depender de a pessoa informar a chave
