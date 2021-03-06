﻿---
title: Set-SPWOPIZone
TOCTitle: Set-SPWOPIZone
ms:assetid: bc751cc4-8ac8-45f7-b6ea-da6fcb5473ac
ms:mtpsurl: https://technet.microsoft.com/fr-fr/library/JJ219451(v=office.15)
ms:contentKeyID: 49645237
ms.date: 12/22/2017
mtps_version: v=office.15
ms.translationtype: HT
---

# Set-SPWOPIZone

 

_**Sapplique à :**Office Web Apps, SharePoint Foundation 2013, SharePoint Server 2013_

_**Dernière rubrique modifiée :**2015-03-09_

Configure la zone que la batterie de serveurs SharePoint actuelle utilisera pour diriger le navigateur vers l'application WOPI.

## Syntaxe

    Set-SPWOPIZone [[-Zone] <String>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]

## Description détaillée

La cmdlet **Set-SPWOPIZone** configure la zone que la batterie de serveurs SharePoint actuelle utilisera pour diriger le navigateur vers l'application WOPI (tel qu'un serveur exécutant l'Office Web Apps Server). La page SharePoint Server du navigateur crée un cadre qui contient une page sur l'application WOPI. La zone pour l'URL de la page d'application WOPI est déterminée par ce paramètre.

Si vous ne spécifiez pas cette zone, la valeur par défaut est internal-HTTPS. Si vous sélectionnez une zone qui n'est pas prise en charge par l'application WOPI, l'Office Web Apps ne fonctionnera pas. Utilisez uniquement HTTP lorsque vous êtes sur un réseau entièrement sécurisé qui utilise IPSEC (chiffrement complet) ou dans un environnement de test qui ne contient pas de données sensibles.

SharePoint Management Shell

## Paramètres


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Paramètre</th>
<th>Obligatoire</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Zone</strong></p></td>
<td><p>Facultatif</p></td>
<td><p>System.String</p></td>
<td><p>Spécifie la zone. Pour obtenir une liste des zones prises en charge par l'application WOPI, exécutez <strong>Get-SPWOPIBinding</strong>.</p>
<p>Si vous avez une batterie de serveurs SharePoint qui est interne et externe, spécifiez externe. Si votre batterie de serveurs SharePoint est uniquement interne, spécifiez interne. Utilisez uniquement HTTP lorsque vous êtes sur un réseau entièrement sécurisé qui utilise IPSEC (chiffrement complet) ou dans un environnement de test qui ne contient pas de données sensibles. Les options sont les suivantes :</p>
<p>- Internal-HTTP</p>
<p>- Internal-HTTPS</p>
<p>- External-HTTP</p>
<p>- External-HTTPS</p></td>
</tr>
<tr class="even">
<td><p><strong>AssignmentCollection</strong></p></td>
<td><p>Facultatif</p></td>
<td><p>Microsoft.SharePoint.PowerShell.SPAssignmentCollection</p></td>
<td><p>Gère les objets de manière à optimiser leur libération. L’utilisation d’objets, tels que <strong>SPWeb</strong> ou <strong>SPSite</strong>, peut consommer des quantités de mémoire élevées et le recours à ces objets dans des scripts Windows PowerShell implique une gestion appropriée de la mémoire. À l’aide de l’objet <strong>SPAssignment</strong>, vous pouvez affecter des objets à une variable et les libérer dès qu’ils ne sont plus nécessaires afin de libérer de la mémoire. Lorsque les objets <strong>SPWeb</strong>, <strong>SPSite</strong> ou <strong>SPSiteAdministration</strong> sont utilisés, ils sont automatiquement libérés si un ensemble d’affectations ou si le paramètre <strong>Global</strong> n’est pas utilisé.</p>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="images/JJ219459.note(Office.15).gif" title="Remarque" alt="Remarque" /><strong>Remarque :</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lorsque le paramètre <strong>Global</strong> est utilisé, tous les objets sont contenus dans le magasin global. Si des objets ne sont pas utilisés immédiatement ou libérés à l’aide de la commande <strong>Stop-SPAssignment</strong>, un scénario d’insuffisance de mémoire peut se produire.</td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><p><strong>Confirm</strong></p></td>
<td><p>Facultatif</p></td>
<td><p>System.Management.Automation.SwitchParameter</p></td>
<td><p>Vous demande confirmation avant d’exécuter la commande. Pour plus d’informations, entrez la commande suivante : <strong>get-help about_commonparameters</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>WhatIf</strong></p></td>
<td><p>Facultatif</p></td>
<td><p>System.Management.Automation.SwitchParameter</p></td>
<td><p>Affiche un message qui explique l’effet de la commande au lieu de l’exécuter. Pour plus d’informations, entrez la commande suivante : <strong>get-help about_commonparameters</strong>.</p></td>
</tr>
</tbody>
</table>


## Types d’entrées

## Types de retours

## Exemple

\--------------EXEMPLE-----------------

    Set-SPWOPIZone -Zone "external-https"

Cet exemple montre comment configurer la batterie de serveurs SharePoint actuelle pour utiliser les connexions externes via HTTPS vers l'application WOPI (tel qu'un serveur exécutant l'Office Web Apps Server).

## Voir aussi


[Get-SPWOPIZone](get-spwopizone.md)  


[Feuille de route de contenu pour Office Web Apps](content-roadmap-for-office-web-apps-server.md)  
[Utiliser Office Web Apps avec SharePoint 2013](use-office-web-apps-with-sharepoint-2013.md)

