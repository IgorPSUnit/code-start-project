Este projeto é um site estático (landing page) para demonstrar o uso do Bootstrap 5.3.8 via CDN, cobrindo layout responsivo, componentes prontos e formulários. A página está organizada em seções com âncoras no menu, e inclui recursos interativos do Bootstrap (modal, dropdown, accordion e carousel).

Estrutura e dependências
Bootstrap CSS via CDN (bootstrap@5.3.8).
CSS próprio via style.css (referenciado no <head>).
Bootstrap JS + Popper via CDN (necessários para dropdown, modal, collapse/accordion, carousel).
Assets locais usados na UI:
./assets/logo.svg
./assets/business.jpg
/assets/banner-1.png, /assets/banner-2.png (no carousel)
Ícones/imagens de cards e projetos (personalizado.png, cliente.png, etc.)
O que a página implementa (seção por seção)
1) Modal de orçamento (#orcamentoModal)
Componente Modal do Bootstrap (.modal, .modal-dialog, .modal-content).
Contém um formulário em grid (.row.g-3) com:
Nome, Email (com required)
Instagram com input-group e prefixo @
Ramo do negócio
Select de plano (Platinum/Gold)
Select de porte da empresa
Botões no rodapé: Cancelar (fecha modal) e Salvar (sem ação JS, apenas UI).
2) Header / Navbar
Navbar responsiva (navbar-expand-lg) com tema escuro (bg-dark e data-bs-theme="dark").
Menu com links âncora para seções (#steps, #benefits, #plans, #projects, #faq).
Dropdown “Planos” (componente Dropdown do Bootstrap).
Botão “Solicitar orçamento” abre o modal via data-bs-toggle="modal".
3) Banner (hero) (#banner)
Layout em grid: texto (CTA) + imagem (business.jpg).
Uso de utilitários de layout: d-flex, flex-column, justify-content-center, fw-bold, w-100.
4) Etapas (#steps)
Seção com título e 3 colunas responsivas (col-sm-12 col-md-4).
Cada coluna traz um ícone SVG inline + título + texto + link.
5) Carousel/Slider (#slider)
Componente Carousel (.carousel.slide) com:
indicadores (botões)
2 slides com imagens
controles anterior/próximo
Observação de código: os dois botões indicadores estão com class="active" (normalmente só o primeiro fica active).
6) Benefícios (#benefits)
Grade de cards (Bootstrap Card) com 6 itens.
Cada card: imagem centralizada + título + descrição + botão “Saiba mais”.
Aqui há um detalhe: foi usado class="containter" (typo). O correto é container (isso afeta o espaçamento/alinhamento padrão do Bootstrap).
7) Planos (#plans)
Seção escura (tema dark) com 2 colunas (Platinum e Gold), cada uma com:
Card
Lista de benefícios usando list-group
Botão “Fazer Orçamento”
Observação: em alguns pontos há texto como “Sistema we” (parece ser “Sistema web”).
8) FAQ (#faq)
Componente Accordion (.accordion) com 3 perguntas.
Corpo das respostas ainda está com texto placeholder em inglês (“This is the second item’s…”), típico de exemplo do Bootstrap.
9) Projetos (#projects)
Seção escura com grid responsiva (col-sm-12 col-lg-4) exibindo 6 cards simples (imagem + legenda).
Usa uma classe custom project-img (provavelmente definida no style.css).
10) Contato (#contact)
Formulário em grid (campos semelhantes ao modal) + botão “Enviar”.
Bloco final com informações de endereço/telefone/email usando layout flex responsivo (flex-column flex-md-row).
11) Footer
Rodapé escuro com navegação por âncoras e texto de copyright “© 2026”.
Componentes Bootstrap demonstrados
Modal
Navbar + Collapse (menu mobile)
Dropdown
Grid system (container/row/col responsivo)
Cards
List Group
Carousel
Accordion (Collapse)
Forms (form-control, form-select, input-group, validação HTML via required)
Utilities (spacing, flex, text, borders)
