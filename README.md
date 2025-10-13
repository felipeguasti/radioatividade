# RadioAtividade - Site Educacional

Projeto educacional interativo para a eletiva RadioAtividade, explorando a história e o impacto do rádio na comunicação.

## 📁 Estrutura do Projeto

```
radioatividade/
├── index.html      # Hub principal com listagem de aulas
├── aula-01.html    # Aula 1: Terror no Rádio
├── aula-02.html    # Aula 2: Comédia e Esportes no Rádio
├── aula-03.html    # Aula 3: Podcasts - O Rádio Moderno
├── aula-04.html    # Aula 4: Rádio e Música
├── aula-05.html    # Aula 5: Jornalismo no Rádio
└── README.md       # Este arquivo
```

## 🚀 Como Usar

### Abertura Local

1. **Baixe todos os arquivos** para uma pasta no seu computador
2. **Abra o arquivo `index.html`** em qualquer navegador moderno:
   - Chrome, Firefox, Edge, Safari, etc.
   - Basta dar duplo clique no arquivo ou arrastar para o navegador
3. **Navegue pelas aulas** clicando nos cards
4. **Seu progresso é salvo automaticamente** no navegador (localStorage)

### Navegação nos Slides

- **No Hub (index.html)**: Clique nos cards das aulas para acessá-las
- **Nas Aulas (Formato Slide)**:
  - Use os botões "← Anterior" e "Próximo →" na parte inferior
  - Use as teclas de seta do teclado (← →)
  - Clique nos pontos indicadores no topo para ir direto a um slide
  - Pressione Home para ir ao primeiro slide
  - Pressione End para ir ao último slide
  - Clique no botão "🏠 Hub" para voltar ao menu principal
- **Progresso**: Acompanhe seu progresso nas barras indicadoras e pontos no topo de cada aula

## 🎬 Como Trocar os Vídeos

### Vídeos do YouTube

Cada aula tem um vídeo embutido. Para trocar o vídeo:

1. **Localize o bloco do vídeo** no arquivo HTML:
```html
<div class="video-poster" id="video-poster" 
     data-video-id="ozbNL3nfWeo"    <!-- ID do vídeo -->
     data-start="30"                 <!-- Início em segundos -->
     data-end="120"                  <!-- Fim em segundos -->
```

2. **Substitua o ID do vídeo**:
   - Pegue a URL do YouTube: `https://www.youtube.com/watch?v=ABC123XYZ`
   - O ID é a parte após `v=`: `ABC123XYZ`
   - Substitua em `data-video-id="ABC123XYZ"`

3. **Ajuste o trecho (opcional)**:
   - `data-start="30"` - início em segundos (ex: 30 = 0:30)
   - `data-end="120"` - fim em segundos (ex: 120 = 2:00)
   - **Importante**: Mantenha trechos de até 90 segundos para melhor experiência

4. **Troque a imagem de poster (opcional)**:
```html
style="background-image: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), 
       url('SUA_URL_AQUI');"
```

### Vídeos Locais (MP4)

Se preferir usar vídeos locais em vez do YouTube:

1. **Salve o vídeo** na mesma pasta dos arquivos HTML
2. **Substitua o bloco do vídeo** por:
```html
<video controls style="width: 100%; border-radius: 10px;">
    <source src="seu-video.mp4" type="video/mp4">
    Seu navegador não suporta vídeo HTML5.
</video>
```

## 🖼️ Como Trocar as Imagens

### Imagens de Poster dos Vídeos

Localize a linha com `background-image` e substitua a URL:

```html
style="background-image: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), 
       url('https://sua-imagem-aqui.jpg');"
```

### Fontes Recomendadas de Imagens (Gratuitas e Livres)

1. **Unsplash** (https://unsplash.com)
   - Imagens de alta qualidade
   - Licença gratuita para uso educacional
   - Exemplos usados no projeto:
     - Rádio vintage: `https://images.unsplash.com/photo-1478737270239-2f02b77fc618`
     - Microfone: `https://images.unsplash.com/photo-1487537708572-3c850b5e856e`

2. **Wikimedia Commons** (https://commons.wikimedia.org)
   - Imagens históricas e educacionais
   - Domínio público e Creative Commons
   - Ideal para conteúdo histórico sobre rádio

3. **Pexels** (https://www.pexels.com)
   - Fotos e vídeos gratuitos
   - Licença livre para uso educacional

4. **Pixabay** (https://pixabay.com)
   - Imagens e ilustrações gratuitas
   - Sem necessidade de atribuição

### Como Obter URL de Imagem

1. Acesse o site (Unsplash, Pexels, etc.)
2. Encontre a imagem desejada
3. Clique com botão direito → "Copiar endereço da imagem"
4. Cole a URL no código HTML

## ⚙️ Funcionalidades Implementadas

### ✅ Requisitos Técnicos

- ✅ Arquivos HTML únicos e autocontidos (CSS e JS inline)
- ✅ Funcionam localmente sem servidor
- ✅ Responsivos (mobile, tablet, desktop)
- ✅ Navegação por teclado (← → para mudar de aula)
- ✅ Acessibilidade (aria-labels, roles, tabindex)
- ✅ Compatível com leitores de tela

### ✅ Funcionalidades Pedagógicas

- ✅ Vídeos com lazy-load (carregam só quando clicados)
- ✅ Trechos de até 90 segundos
- ✅ 3 perguntas interativas por aula
- ✅ Feedback imediato para cada resposta
- ✅ Botão "Revelar resposta" em cada pergunta
- ✅ Curiosidades históricas com fontes
- ✅ Área de comentários/ideias para rádio escolar
- ✅ Salvamento automático de progresso (localStorage)
- ✅ Indicadores visuais de progresso

### ✅ Design e Estética

- ✅ Tema RadioAtividade (retro + moderno)
- ✅ Paleta de cores: marrom escuro, creme, âmbar, ciano
- ✅ Ondas sonoras animadas
- ✅ Ícones temáticos (📻 🎙️ 📡)
- ✅ Textura de grão no fundo
- ✅ Animações suaves e transições

## 💾 Sistema de Progresso

O site salva automaticamente:
- ✅ Perguntas respondidas
- ✅ Acertos e erros
- ✅ Aulas concluídas
- ✅ Comentários e ideias dos alunos

**Dados salvos em**: localStorage do navegador (não precisa de servidor)

### Como Limpar o Progresso

Para resetar o progresso de um aluno:
1. Abra o Console do navegador (F12)
2. Digite: `localStorage.clear()`
3. Pressione Enter
4. Recarregue a página (F5)

## 🎨 Personalização do Tema

### Cores Principais

Para alterar as cores do tema, procure por estas variáveis no CSS:

```css
/* Cores do tema RadioAtividade */
#3b2f2f  /* Marrom escuro (fundo) */
#f3e9de  /* Creme (texto) */
#d4a15b  /* Âmbar (destaques) */
#00c8d7  /* Ciano elétrico (acentos) */
```

### Fontes

O projeto usa fontes web-safe (não requer downloads):
- **Títulos**: Impact, Arial Black
- **Corpo**: Segoe UI, Tahoma, Verdana

## 📱 Compatibilidade

### Navegadores Suportados
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Opera 76+

### Dispositivos
- ✅ Desktop (Windows, Mac, Linux)
- ✅ Tablets (iPad, Android)
- ✅ Smartphones (iOS, Android)

## 📋 Licenciamento e Uso Educacional

### Conteúdo do Projeto
- **Código**: Livre para uso educacional
- **Modificações**: Permitidas e encorajadas
- **Distribuição**: Livre para escolas e educadores

### Recursos Externos
- **Vídeos do YouTube**: Uso educacional (Fair Use)
  - Manter link para fonte original
  - Usar apenas trechos curtos (≤90s)
  - Não fazer download ou redistribuição

- **Imagens do Unsplash**: Licença Unsplash
  - Uso gratuito para fins educacionais
  - Não requer atribuição (mas é recomendado)

- **Imagens do Wikimedia Commons**: 
  - Verificar licença específica de cada imagem
  - Preferir Public Domain ou CC BY

## 🔧 Solução de Problemas

### Vídeo não carrega
- Verifique se o ID do vídeo está correto
- Confirme se o vídeo está disponível no YouTube
- Teste a URL diretamente no navegador

### Progresso não salva
- Verifique se o navegador permite localStorage
- Não use modo anônimo/privado
- Limpe o cache se necessário

### Layout quebrado no mobile
- Verifique se a viewport está configurada
- Teste em diferentes tamanhos de tela
- Use as ferramentas de desenvolvedor (F12)

## 📞 Suporte

Para dúvidas ou problemas:
1. Verifique este README primeiro
2. Consulte os comentários no código HTML
3. Teste em diferentes navegadores
4. Verifique o Console do navegador (F12) para erros

## 🎓 Uso em Sala de Aula

### Sugestões de Aplicação

1. **Aula Presencial**:
   - Projete o site no datashow
   - Navegue pelas aulas com os alunos
   - Discuta as respostas em grupo

2. **Aula Remota**:
   - Compartilhe os arquivos via Google Drive/OneDrive
   - Alunos acessam localmente em seus computadores
   - Progresso individual salvo automaticamente

3. **Atividade Assíncrona**:
   - Disponibilize os arquivos para download
   - Alunos completam no seu ritmo
   - Comentários salvos podem ser compartilhados depois

### Avaliação

O sistema salva:
- Número de perguntas respondidas
- Acertos e erros
- Ideias propostas pelos alunos

Para acessar os dados salvos (Console F12):
```javascript
// Ver progresso da Aula 01
console.log(localStorage.getItem('radioatividade_aula_01'));

// Ver progresso da Aula 02
console.log(localStorage.getItem('radioatividade_aula_02'));
```

## 🚀 Próximos Passos

Para expandir o projeto:

1. **Adicionar mais aulas**:
   - Copie `aula-02.html`
   - Renomeie para `aula-03.html`
   - Atualize o conteúdo
   - Adicione card no `index.html`

2. **Criar exercícios práticos**:
   - Gravação de áudio
   - Roteiros de programas
   - Análise de podcasts

3. **Adicionar recursos multimídia**:
   - Áudios de programas históricos
   - Galeria de imagens
   - Timeline interativa

---

**Projeto RadioAtividade** - Educação através da história do rádio 📻
*Desenvolvido para uso educacional - 2025*