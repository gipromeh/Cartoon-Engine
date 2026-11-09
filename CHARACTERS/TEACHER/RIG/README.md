# Teacher 2.5D Rig — технический план

Статус: SPECIFICATION / NOT IMPLEMENTED.

Цель — квази-3D шарнирный персонаж с объёмными сегментами, кинематической иерархией и возможностью дальнейшего перехода к единой деформируемой сетке.

## Сегменты

- head, neck, torso, pelvis
- upper_arm.L / upper_arm.R
- forearm.L / forearm.R
- hand.L / hand.R
- thigh.L / thigh.R
- shin.L / shin.R
- foot.L / foot.R

## Суставы

- neck
- shoulder.L / shoulder.R
- elbow.L / elbow.R
- wrist.L / wrist.R
- hip.L / hip.R
- knee.L / knee.R
- ankle.L / ankle.R

Для каждого сустава определить pivot, локальные оси, нейтральную позу и пределы вращения. Для кистей подготовить состояния relaxed, reaching, gripping, supporting, pointing, presenting.

## Контроллеры

- IK target для каждой кисти;
- pole target для локтя;
- attachment / parent constraint для предмета в захвате;
- контроллер головы и направления взгляда;
- контроллер таза и стоп.

## Критерии прототипа

1. Поворот и наклон головы.
2. Поднятие руки и сгибание локтя.
3. Дотягивание до камня через IK.
4. Захват и перенос камня.
5. Показ камня перед собой.
6. Отсутствие щелей и нарушения силуэта в front, 3/4 и profile.

Дизайн персонажа менять нельзя: rig обязан соответствовать REFERENCE v1.0.
