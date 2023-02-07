# Consultas SQL
Projeto desenvolvido por:

Jozilene Serafin
Katarine Melo
Lais Leão
Lidiane Celina
Nilton de Maria


## Pergunta 1: Quantas variações de cores existem na base LEGO e quantas são utilizadas?

SELECT COUNT(DISTINCT color_id) FROM inventory_parts;

## Pergunta 2: Qual foi o ano e quais são os primeiros temas criados na base de dados?

SELECT MIN(year) FROM sets_1;

SELECT * FROM sets_1 WHERE year=1955;

## Pergunta 3: Qual nome e o id da categoria da peça Minifig Hair Tousled?

SELECT part_categories.name, parts_1.part_cat_id, parts_1.name
FROM part_categories
INNER JOIN parts_1
ON part_categories.id = parts_1.parts_1.part_cat_id AND parts_1.name="Minifig Hair Tousles"

## Pergunta 4: Quantas variações de peças têm na categoria "Brincks Special"?

SELECT * FROM part_categories WHERE name="Brinks Special";

SELECT COUNT(part_cat_id) FROM parts_1 WHERE part_cat_id=5;

## Pergunta 5: Qual a quantidade de inventory set no tema 58?

SELECT * FROM sets_1 WHERE theme_id=58;
