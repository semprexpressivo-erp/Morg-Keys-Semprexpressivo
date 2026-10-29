# Morg Keys: versão Semprexpressivo

Este repositório é um **fork** do [Morg Keys](https://github.com/Carlobks/Morg-Keys) para os PCs da Semprexpressivo. Só acrescenta a **animação de arranque com o logótipo da empresa**. Todo o resto é o Morg Keys original.

## O que muda em relação ao original

Tudo o que é da empresa está marcado com `SXP-LOCAL`:

```powershell
git grep -n SXP-LOCAL
```

| Ficheiro | O que tem |
|---|---|
| `2-configuracao\glzr\zebar\omarchy-catppuccin\arranque\sxp.bmp` | 1.º quadro do logótipo (576×214), mostrado pela cortina nativa |
| `…\arranque\splash.html` | O desenho (SVG) e o ciclo da animação `sxp` |
| `…\morg_config_arranque.py` | `ANIMACOES["sxp"]` |
| `…\guia\sistema.html` | O nome "SXP" no painel `Alt+Esc` |
| `…\guia\arranque.txt`, `scripts\arranque-modelo.txt` | O comentário "cafe \| sxp" |
| `scripts\gerar-modelos.ps1` | O `sxp.bmp` na lista do pacote |
| `scripts\instalar.ps1` | A animação por omissão é `sxp` (no original é `cafe`) |
| `VERSAO-SEMPREXPRESSIVO.md` | Este ficheiro |

A animação foi acrescentada pela receita 5b de `docs\receitas.md`. O café continua disponível: `Alt+Esc`, tocar `E`.

## Regras

- **Nada daqui vai para o Morg Keys original.** O original não tem marcas nem dados de empresas (`docs\decisoes\0002-repositorio-publico-sem-marca.md`). Correções genéricas fazem-se num ramo à parte, a partir do `main` do original, e seguem para lá por pull request, sem nenhuma linha `SXP-LOCAL`.
- **Receber atualizações do original:** no GitHub, "Sync fork". Na linha de comandos:
  ```
  git fetch upstream
  git merge upstream/main
  ```
  Os conflitos, se houver, são só nas linhas `SXP-LOCAL`.
- **Instalar num PC da empresa:**
  1. descarregar este repositório (Code > Download ZIP);
  2. duplo clique em `INSTALAR.cmd`, no Explorador e nunca a partir de um terminal do Claude Code (armadilha A2).

  Se o PC já tinha a versão antiga (pasta `~\.glzr`), o instalador traz as apps, o arranjo das janelas e os `.bat` de arranque.
