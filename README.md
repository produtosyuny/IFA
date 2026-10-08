# Ọ̀nà Yorùbá — Ifá e Língua

Aplicação web estática para estudar e organizar língua Yorùbá e Ifá.

## Executar

```bash
python3 -m http.server 3000 --bind 0.0.0.0
```

Abra `http://localhost:3000`.

## Expandir a árvore

Edite `content.json`. Cada item pode receber:

- `summary`
- `pronunciation`
- `translations`
- `explanation`
- `uses`
- `phrases`
- `context`
- `variations`
- `related`
- `exercises`
- `sources`
- `cards`

Campos ainda não desenvolvidos devem permanecer vazios (`""` ou `[]`). A interface renderiza esses espaços como “Em construção” e não inventa conteúdo.

O progresso é salvo apenas no `localStorage` do navegador.

## Revisão

Cada conceito tem um campo `review`:

```json
"review": { "claude": "ok | corrigido | pendente", "confianca": "alta | media", "nota": "", "manus": null, "gemini": null, "humano": null }
```

- `pendente` = prioridade para validação humana (Ya/baba).
- A interface só mostra **validado** quando `humano` estiver preenchido.
- A chave de pronúncia fica em `project.pronunciationKey`.
