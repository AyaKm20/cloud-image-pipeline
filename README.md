# Packer Cloud Image Automation with GitHub Actions

Ce projet automatise la création d'images cloudisées pour KVM en utilisant Packer, Cloud-init et GitHub Actions.

## Structure du projet

- `.github/workflows/build.yml` : Configuration de GitHub Actions pour exécuter Packer et créer des images.
- `template.json` : Fichier Packer pour la construction des images cloudisées.
- `user-data` : Configuration Cloud-init pour l'initialisation de la machine virtuelle.
- `meta-data` : Métadonnées de l'instance pour Cloud-init.

## Environnements pris en charge
- `dev`
- `test`
- `prod`

## Prérequis

1. [Packer](https://www.packer.io/)
2. [GitHub Actions](https://docs.github.com/en/actions)
3. Clé privée SSH (stockée dans les secrets GitHub)

## Installation

1. Clonez ce repository.
2. Ajoutez vos secrets SSH dans GitHub Secrets.
3. Faites un push ou une pull request pour démarrer l'automatisation.

## GitHub Actions

Les workflows sont exécutés à chaque push vers la branche `main` ou pull request vers `main`. L'automatisation couvre la construction des images pour les environnements `dev`, `test` et `prod`.
