# 🎬 YouTube Video Downloader

[![CI/CD Pipeline](https://github.com/baku01/youtube_video_downloader/workflows/CI%2FCD%20Pipeline/badge.svg)](https://github.com/baku01/youtube_video_downloader/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Rust](https://img.shields.io/badge/rust-1.70+-orange.svg)](https://www.rust-lang.org)
[![Platform](https://img.shields.io/badge/platform-Linux%20%7C%20macOS%20%7C%20Windows-lightgrey)](https://github.com/baku01/youtube_video_downloader)

Um downloader de vídeos do YouTube moderno e eficiente, escrito em Rust, com interface de linha de comando interativa e animações dinâmicas.

## ✨ Características

- 🚀 **Interface Interativa**: Modo interativo com animações coloridas e efeitos visuais
- 🎥 **Download de Vídeo**: Suporte a vídeos em alta qualidade (até 720p)
- 🎵 **Download de Áudio**: Extração de áudio em formato MP3 (192K)
- 🔗 **URLs Flexíveis**: Suporte a youtube.com, youtu.be, m.youtube.com e shorts
- ⚡ **Performance**: Implementado em Rust para máxima eficiência
- 🎨 **Animações**: Efeitos visuais incluindo matrix, spinner, progress bar e typing
- 🛠️ **Auto-instalação**: Instalação automática do yt-dlp quando necessário
- 📊 **Estatísticas**: Acompanhamento de downloads da sessão
- 🎭 **ASCII Art**: Arte ASCII aleatória com temas brasileiros

## 🚀 Instalação

### Pré-requisitos

- [Rust](https://rustup.rs/) (versão 1.70 ou superior)
- [Python 3](https://www.python.org/downloads/) (para yt-dlp)
- [pip3](https://pip.pypa.io/en/stable/installation/) (geralmente incluído com Python)

### Instalação via Cargo

```bash
# Clone o repositório
git clone https://github.com/baku01/youtube_video_downloader.git
cd youtube_video_downloader

# Compile e instale
cargo build --release

# Ou execute diretamente
cargo run
```

### Instalação via Binário

Baixe o binário pré-compilado da [página de releases](https://github.com/baku01/youtube_video_downloader/releases).

## 📖 Uso

### Modo Linha de Comando

```bash
# Download de vídeo
./youtube_video_downloader "https://www.youtube.com/watch?v=dQw4w9WgXcQ" -o "meu_video"

# Download apenas de áudio
./youtube_video_downloader "https://www.youtube.com/watch?v=dQw4w9WgXcQ" -o "meu_audio" --audio-only

# Modo interativo
./youtube_video_downloader --interactive
```

### Modo Interativo

O modo interativo oferece uma experiência rica com animações e comandos especiais:

```
🎬 YouTube Video Downloader - Modo Interativo

Comandos disponíveis:
• exit/quit - Sair do programa
• help - Mostrar ajuda
• clear - Limpar tela
• stats - Mostrar estatísticas
• demo - Demonstração de animações
• download <url> [nome] - Download direto
• Cole uma URL do YouTube para download automático

ytdl> https://www.youtube.com/watch?v=dQw4w9WgXcQ
```

### Opções da Linha de Comando

```
OPÇÕES:
    -o, --output <NOME>     Nome do arquivo de saída
    -a, --audio-only        Download apenas do áudio (MP3)
    -i, --interactive       Modo interativo
    -h, --help             Mostrar ajuda
    -V, --version          Mostrar versão
```

## 🎨 Recursos Visuais

### Animações Disponíveis

- **Matrix Effect**: Efeito chuva de código estilo Matrix
- **Spinner**: Indicadores de carregamento animados
- **Progress Bar**: Barras de progresso coloridas
- **Typing Animation**: Efeito de digitação
- **ASCII Art**: Arte ASCII temática brasileira

### Temas de ASCII Art

- 🇧🇷 Bandeira do Brasil
- ⚽ Futebol brasileiro
- 🎵 Música brasileira (Raul Seixas, etc.)
- 🏛️ Monumentos (Cristo Redentor)
- 🎬 Cinema brasileiro

## 🛠️ Desenvolvimento

### Estrutura do Projeto

```
youtube_video_downloader/
├── src/
│   └── main.rs              # Código principal
├── .github/
│   └── workflows/
│       ├── ci.yml           # Pipeline CI/CD
│       ├── integration.yml  # Testes de integração
│       └── release.yml      # Gerenciamento de releases
├── Cargo.toml              # Dependências Rust
├── README.md               # Este arquivo
└── LICENSE                 # Licença MIT
```

### Dependências Principais

- `clap`: Interface de linha de comando
- `colored`: Texto colorido
- `crossterm`: Controle de terminal
- `regex`: Expressões regulares
- `rustyline`: Editor de linha interativo
- `tokio`: Runtime assíncrono
- `rand`: Geração de números aleatórios

### Executando Testes

```bash
# Testes unitários
cargo test

# Testes com cobertura
cargo install cargo-llvm-cov
cargo llvm-cov

# Linting
cargo clippy --all-targets --all-features

# Formatação
cargo fmt
```

### Benchmarks

```bash
# Instalar cargo-criterion
cargo install cargo-criterion

# Executar benchmarks
cargo criterion
```

## 🤝 Contribuindo

1. **Fork** o projeto
2. Crie uma **branch** para sua feature (`git checkout -b feature/AmazingFeature`)
3. **Commit** suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. **Push** para a branch (`git push origin feature/AmazingFeature`)
5. Abra um **Pull Request**

### Diretrizes de Contribuição

- Siga as convenções de código Rust
- Adicione testes para novas funcionalidades
- Mantenha a documentação atualizada
- Use commits semânticos
- Certifique-se de que todos os testes passam

## 📋 Roadmap

- [ ] Suporte a playlists
- [ ] Interface gráfica (GUI)
- [ ] Suporte a mais plataformas de vídeo
- [ ] Download paralelo
- [ ] Configuração via arquivo
- [ ] Plugin system
- [ ] Integração com gerenciadores de download

## 🐛 Problemas Conhecidos

- Alguns vídeos podem não estar disponíveis devido a restrições geográficas
- A qualidade máxima depende da disponibilidade no YouTube
- Requer conexão com a internet para verificar atualizações do yt-dlp

## 📄 Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.

## 🙏 Agradecimentos

- [yt-dlp](https://github.com/yt-dlp/yt-dlp) - Motor de download
- [Rust Community](https://www.rust-lang.org/community) - Linguagem e ecossistema
- [Clap](https://github.com/clap-rs/clap) - Interface de linha de comando
- [Crossterm](https://github.com/crossterm-rs/crossterm) - Controle de terminal multiplataforma

## 📞 Suporte

- 🐛 [Issues](https://github.com/baku01/youtube_video_downloader/issues)
- 💬 [Discussions](https://github.com/baku01/youtube_video_downloader/discussions)
- 📧 Email: your.email@example.com

---

<div align="center">
  <strong>Feito com ❤️ e ☕ no Brasil</strong>
</div>
# youtube_video_downloader
