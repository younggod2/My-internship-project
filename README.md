# Проект стажировки в BIOCAD
*Ключевые детали реализации проекта удалены или изменены, чтобы не нарушать NDA.*


Инструмент для предсказания изменения аффинности антитела при замене аминокислоты

## Использование:  
`python3 AffinityTool.py [--clf | --reg]  path2mutations path2pdbs`  

**path2mutations** — путь до таблицы.csv с мутациями, в ней должны быть колонки 'PDB', 'chain' и 'mutation' в формате *WTnumMUT*, где  
*WT* – исходная АК  
*num* — номер исходной АК в цепи (может содержать букву - 103A)  
*MUT* – АК, на которую происходит мутация  
*WT* и *MUT* могут быть трехбуквенные и однобуквенные, регистр не важен  
**path2pdbs** — путь до папки с .pdb файлами белков

Пример:  
`python3 AffinityTool.py --clf '/Users/chekalin/Desktop/AffinityTool/example_mutation.csv' './datasets/SiPMAB'`

Output: безвредная(0) или вредная(1) мутация

## Описание
datasets — экспериментальные данные об изменении аффинности при мутации  
feature_eng — выделение признаков из тренировочных данных  
model — обучение модели



