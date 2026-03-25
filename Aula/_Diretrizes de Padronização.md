# Diretrizes de Padronização de Notas

## 1. Estrutura do Arquivo

- Logo abaixo do título (incluso por padrão, não precisa criar), incluir um bloco de metadados com `Professor`, `Data` e `Tags` (se aplicável):

```
**Professor:** Nome  
**Data:** DD/MM/AAAA  
**Tags:** `tag1` `tag2`
```

- Cada grande tópico da aula usa `## ` (H2).
- Subtópicos usam `### ` (H3).
- Evitar profundidade maior que H3. Se necessário, usar listas aninhadas.

---

## 2. Formatação de Texto

- **Negrito** (`**texto**`) para termos técnicos, siglas e conceitos-chave na primeira ocorrência.
- *Itálico* (`*texto*`) para ênfase secundária ou estrangeirismos.
- `Código inline` (`` `texto` ``) para nomes de variáveis, pinos, funções, formatos (ex: `T#5S`, `CV`, `Q`).
- Nunca misturar negrito e itálico desnecessariamente.

---

## 3. Listas

- Usar listas com marcador (`-`) para itens sem ordem relevante.
- Usar listas numeradas (`1.`) para passos sequenciais ou prioridades.
- Cada item da lista deve ser uma frase ou fragmento claro e consistente — não misturar frases completas com palavras soltas na mesma lista.
- Listas de parâmetros de blocos (timers, contadores etc.) seguem o padrão:

```
- **SIGLA:** Descrição curta e objetiva.
```

---

## 4. Tabelas

- Toda tabela deve ter cabeçalhos descritivos (ex: `| Entrada A | Entrada B | Saída |`).
- Alinhar colunas com espaços para legibilidade no raw.
- Tabelas verdade: sempre com colunas nomeadas `A`, `B`, `Saída` (ou conforme a lógica).

---

## 5. Fórmulas Matemáticas

- Fórmulas inline: `$formula$`
- Fórmulas em bloco (display): `$$formula$$`
- Usar LaTeX padrão. Evitar `\Large` e outros modificadores de tamanho desnecessários dentro de `$$`.
- Nomear a fórmula com um título `### ` acima quando ela representar um conceito específico.

---

## 6. Imagens e Arquivos de Mídia

- Imagens são referenciadas com `![Descrição alt](caminho)`.
- A descrição alt deve ser breve e descritiva (ex: `![Diagrama porta AND](../MEDIA/porta_and.png)`).
- PDFs e outros documentos embutidos são referenciados com `![Descrição](caminho.pdf)` e precedidos de um título explicativo.
- Não deixar imagens ou PDFs sem contexto — sempre precedê-los de um parágrafo ou título que explique o que é.

---

## 7. Lembretes e Avisos

- Usar blockquote (`>`) para avisos importantes, lembretes de aula ou observações do professor:

```
> **Lembrete:** Levar componentes na próxima aula.
```

---

## 8. Exercícios

- A seção de exercícios usa `## Exercícios` (H2).
- Cada exercício é identificado por letra ou número: `### A)`, `### B)` ou `### Exercício 1`.
- PDFs de exercícios são referenciados antes dos itens resolvidos.

---

## 9. Nomenclatura de Arquivos

- Formato: `Aula_NomeDisciplina.md`
- Sem espaços, sem acentos no nome do arquivo.
- Exemplos: `Aula_Automacao.md`, `Aula_Telecom.md`, `Aula_Projetos_II.md`

---

## 10. Exemplo de Estrutura Completa

```markdown
# Nome da Disciplina

**Professor:** Nome do Professor  
**Data:** DD/MM/AAAA  
**Tags:** `tag1` `tag2`

---

## Tópico Principal

Breve introdução ou contexto do tópico.

### Subtópico

Conteúdo...

- **PARAM:** Descrição.

| A | B | Saída |
|---|---|-------|
| 0 | 0 |   0   |

$$
\text{Fórmula}
$$

> **Lembrete:** Observação importante.

## Exercícios

### A)

![Enunciado exercício A](../MEDIA/exercicio_a.png)
```
