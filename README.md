# Design Patterns for Fun and Proficiency in Symfony! 

Well hi there! This repository holds the code and script
for the [Design Patterns for Fun and Proficiency Tutorials](https://symfonycasts.com/screencast/design-patterns) on SymfonyCasts.

## Setup

```
composer install
```

**Running the App!**

```
php bin/console app:game:play
``` 

## Builder

`'fighter' => new Character(90, 12, new TwoHandedSwordType(), new ShieldType()),`

to 

```php
'fighter' => $this->createCharacterBuilder()
    ->setMaxHealth(90)
    ->setBaseDamage(12)
    ->setAttackType('sword')
    ->setArmorType('shield')
    ->buildCharacter(),
```
