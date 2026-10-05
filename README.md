# Agmfood – Site da hamburgueria

Site de uma página para a **Agmfood**, hamburgueria artesanal em Anápolis, GO.
O cliente monta o burger escolhendo o **blend de carne** e o **pão**, vê o resumo do pedido numa comanda e envia tudo pronto pelo **WhatsApp**.

> Este projeto é uma **prévia** feita para mostrar ao dono como ficará o site final.

## Visual

- Fundo preto com detalhes em laranja
- Títulos em **Unbounded**, texto em **Manrope** e comanda em **Space Mono** (Google Fonts)
- Layout responsivo, pensado primeiro para celular
- Animação só quando o cliente troca de opção, e desligada para quem prefere menos movimento

## O que o site tem

- **Montador de burger:** 5 blends e 4 tipos de pão, com resumo do pedido atualizado na hora
- **Pedido pelo WhatsApp:** o botão abre a conversa com a mensagem já escrita, por exemplo: *"Olá! Quero um burger com blend Cupim com bacon no pão Integral."*
- **Como pedir:** salão, retirada e delivery
- **Onde fica:** endereço, horário e botão que abre o Google Maps
- Acessível: botões navegáveis pelo teclado, foco visível e leitura por leitores de tela

## Tecnologias

HTML, CSS e JavaScript puros, num único arquivo. Não precisa de instalação, build nem dependências.

## Estrutura

```
agmfood/
├── index.html   # site completo (HTML + CSS + JS)
└── README.md
```

## Como rodar localmente

1. Baixe ou clone o repositório
2. Abra o `index.html` no navegador

Se preferir um servidor local:

```bash
python -m http.server 8000
```

Depois acesse `http://localhost:8000`.

## Como colocar no ar (Vercel)

1. Suba o projeto para um repositório no GitHub
2. Em [vercel.com](https://vercel.com), clique em **Add New → Project** e importe o repositório
3. Não precisa mudar nenhuma configuração: clique em **Deploy**
4. Para usar um domínio próprio, vá em **Settings → Domains**

Cada novo `git push` publica a atualização automaticamente.

## Como personalizar

Tudo fica no `index.html`.

| O que mudar | Onde |
|---|---|
| Número do WhatsApp | Variável `WHATS` no início do `<script>`. Só dígitos, no formato `55` + DDD + número |
| Blends de carne | Lista `BLENDS` no `<script>` (nome e descrição) |
| Tipos de pão | Lista `PAES` no `<script>` |
| Cores | Variáveis no começo do CSS (`:root`). O laranja é `--or` |
| Endereço e horário | Seções "Onde fica" e "Horário" no HTML |
| Nota do Google | Bloco `.fatos` no topo do HTML |
| Texto "Prévia do site" | Rodapé. **Remova na versão final** |

### Para a versão final

- [ ] Confirmar com o dono a lista completa de pães
- [ ] Adicionar fotos reais dos burgers
- [ ] Incluir cardápio com preços, se ele quiser
- [ ] Adicionar link do Instagram
- [ ] Remover "Prévia do site" do rodapé
- [ ] Conferir se o número informado é WhatsApp antes de publicar

## Observações

- As informações do site (endereço, horário, nota e blends) vieram de dados públicos do Google Maps e devem ser **confirmadas com o dono**.
- Evite fazer testes enviando mensagens no botão de WhatsApp, pois ele abre a conversa real com o restaurante.

## Créditos

Desenvolvido por Wanderson para a Agmfood.
