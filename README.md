# Dados abertos — Monitor de Editais DBSeller

Saída diária da coleta de editais no PNCP. **Somente dados**, atualizado automaticamente
por GitHub Actions em dias úteis às 06:40 (horário de Brasília).

## O arquivo

`dados/editais.json` traz os editais **abertos** (com proposta em recebimento) de sistemas
de gestão pública municipal, com:

- valor estimado, somado item a item — o índice de busca do PNCP não expõe esse campo
- prazo de encerramento e dias restantes
- módulos pedidos pelo órgão, extraídos da lista de itens
- pontuação de prioridade e marcação de dados suspeitos

## Origem e limites

Dados públicos do Portal Nacional de Contratações Públicas, nos termos da Lei 12.527/2011.

O valor estimado é **teto de referência do órgão**, não valor de contratação. A cobertura é
parcial por natureza: órgão que publica apenas em portal próprio não aparece no PNCP.
Registros com valor irrisório ou data de encerramento implausível vêm marcados como
`suspeito` — são erros de preenchimento na origem.
