# 🏁 Supercar Gallery

> **Uma experiência digital dedicada à engenharia, ao design e à performance dos supercarros mais extraordinários do mundo.**

A **Supercar Gallery** é uma galeria interativa de supercarros e hipercarros. O projeto reúne uma interface escura de estética premium, catálogo de veículos, pesquisa e filtros, páginas de detalhes, favoritos, comparação de modelos e uma área administrativa demonstrativa.

Explore máquinas de marcas como Ferrari, Lamborghini, McLaren, Koenigsegg, Aston Martin, Pagani e Rimac — com informações técnicas e imagens organizadas em uma experiência responsiva.

---

## ✨ Visão geral

- **Garagem interativa:** navegue pelo catálogo e descubra os modelos disponíveis.
- **Pesquisa e filtros:** encontre veículos por nome, marca, motorização e categoria; refine a listagem por critérios disponíveis na interface.
- **Detalhes dos veículos:** consulte especificações, desempenho, descrição e imagens de cada modelo.
- **Favoritos:** salve seus carros preferidos para encontrá-los rapidamente.
- **Comparação:** coloque modelos lado a lado para analisar suas características.
- **Área administrativa demonstrativa:** interface para visualizar e gerenciar os dados apresentados no navegador.
- **Experiência responsiva:** layout adaptável a diferentes tamanhos de tela.
- **Imagens otimizadas:** suporte a imagens WebP e processamento de imagens adicionadas pela interface.
- **Animações e microinterações:** transições e efeitos para deixar a navegação mais fluida.

## 🛠️ Tecnologias

| Tecnologia | Utilização |
|---|---|
| HTML5 | Estrutura e conteúdo das páginas |
| CSS3 | Estilos, identidade visual e responsividade |
| JavaScript (Vanilla) | Navegação, catálogo, filtros, favoritos e interações |
| Tailwind CSS | Utilitários de layout e estilização |
| GSAP | Animações e transições |
| Font Awesome | Ícones |
| Google Fonts | Tipografia — Orbitron, Inter e JetBrains Mono |
| JSZip | Recursos de compactação disponíveis na interface |

> **Nota sobre a arquitetura:** a versão presente neste repositório funciona no navegador, com dados do catálogo e favoritos armazenados no `localStorage` e estado de sessão administrativa no `sessionStorage`. A seção “Código Full-Stack” da interface apresenta referências e exemplos de implementação; ela não significa que um servidor Flask ou um banco SQLite estejam sendo executados por este projeto estático. A integração com backend real pode ser desenvolvida em uma etapa futura.

## 🚘 Modelos em destaque

O catálogo inicial inclui modelos como:

- Aston Martin Valkyrie
- Ferrari SF90 Stradale
- Koenigsegg Jesko Absolut
- Lamborghini Revuelto
- McLaren 750S
- Pagani Huayra R
- Rimac Nevera
- Ferrari 499P — destaque visual da página inicial

Os dados e modelos iniciais são definidos em `assets/js/app.js`. A disponibilidade de imagens depende dos arquivos existentes em `assets/images/`.

## 📁 Estrutura do projeto

```text
supercar/
├── assets/
│   ├── css/
│   │   └── style.css
│   ├── images/
│   │   ├── banners/
│   │   ├── icons/
│   │   ├── logos/
│   │   ├── pages/
│   │   └── vehicles/
│   └── js/
│       └── app.js
├── index.html
├── license
└── README.md
```

## 🚀 Como executar

O projeto não exige instalação de dependências ou processo de build para a execução básica.

### Opção 1 — Abrir diretamente

1. Baixe ou clone este repositório.
2. Abra a pasta `supercar`.
3. Abra o arquivo `index.html` no navegador.

### Opção 2 — Usar um servidor local

Se preferir executar com um servidor local, abra o terminal na pasta do projeto e rode:

```bash
python -m http.server 8000
```

Depois, acesse:

```text
http://localhost:8000
```

> Algumas bibliotecas e fontes são carregadas por CDN. Para que esses recursos externos funcionem, é necessária uma conexão com a internet.

## 💾 Persistência dos dados

A versão atual utiliza recursos de armazenamento do próprio navegador:

- `localStorage`: mantém os dados do catálogo e os favoritos no navegador.
- `sessionStorage`: mantém o estado de sessão administrativa durante a sessão da aba.

Esses dados são locais ao navegador e não são sincronizados entre dispositivos ou usuários. Limpar os dados do site no navegador pode removê-los.

## 🧩 Personalização

### Adicionar ou alterar veículos

Os veículos iniciais estão no array `DEFAULT_CARS`, dentro de:

```text
assets/js/app.js
```

Cada veículo utiliza propriedades como:

```js
{
  id: 1,
  name: "SF90 Stradale",
  brand: "Ferrari",
  year: 2024,
  price: 625000,
  engine: "4.0L Twin-Turbo V8 Hybrid",
  horsepower: 986,
  top_speed: 211,
  category: "Hybrid Supercar",
  description: "Descrição do veículo.",
  image_url: "assets/images/vehicles/ferrari-sf90-stradale.webp"
}
```

### Adicionar imagens

1. Coloque a imagem na pasta correspondente dentro de `assets/images/`.
2. Prefira o formato **WebP**, com dimensões adequadas para uso na web.
3. Atualize o caminho em `image_url` no cadastro do veículo.
4. Confira se o nome e a extensão do arquivo correspondem exatamente ao caminho informado.

## 🔮 Próximas evoluções

O projeto pode evoluir para uma aplicação full-stack com:

- API REST para consulta e gerenciamento dos veículos.
- Backend em Python com Flask.
- Banco de dados SQLite ou PostgreSQL.
- Autenticação real, com senhas protegidas e controle de permissões.
- Upload de imagens com armazenamento no servidor.
- Painel administrativo conectado ao banco de dados.
- Testes automatizados e validação de dados no servidor.

Esses itens são possibilidades de evolução e não são apresentados como funcionalidades de backend já implementadas nesta versão.

## 📌 Observações

- Os preços e dados técnicos exibidos têm finalidade demonstrativa e podem não refletir valores ou especificações oficiais atualizados.
- Marcas, nomes e modelos pertencem aos respectivos titulares.
- Bibliotecas, fontes e recursos externos seguem os termos e licenças de seus fornecedores.
- Consulte o arquivo `license` incluído no projeto para informações sobre a licença do código.

---

## 👨‍💻 Autor

Desenvolvido por **Jesi Solutions**.

Se este projeto despertou seu interesse, considere deixar uma ⭐ no repositório e acompanhar as próximas evoluções.

<p align="center">
  <strong>SUPERCAR GALLERY</strong><br>
  <em>Beyond performance. A gallery of automotive excellence.</em>
</p>
