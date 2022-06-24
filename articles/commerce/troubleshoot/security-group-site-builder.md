---
title: Commerce-sivustonmuodostimen käyttöoikeusryhmän määrittäminen ei onnistu ensimmäisen käyttöönoton yhteydessä
description: Tämä artikkeli antaa vianmääritysohjeita, jotka voivat auttaa ongelmassa, jossa Commerce-sivustonmuodostimen Microsoft Azure Active Directory (Azure AD) -suojausryhmä ei näy vaihtoehtona, kun luot sähköisen kaupankäynnin komponentteja Microsoft Dynamics Lifecycle Servicesissä (LCS) uuden sähköisen kaupankäynnin vuokraajan ensimmäisen käyttöönoton yhteydessä.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 797df828df16547eb3aef1f9865a663281fb9224
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899012"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Commerce-sivustonmuodostimen käyttöoikeusryhmän määrittäminen ei onnistu ensimmäisen käyttöönoton yhteydessä

[!include [banner](../../includes/banner.md)]

Tämä artikkeli antaa vianmääritysohjeita, jotka voivat auttaa ongelmassa, jossa Commerce-sivustonmuodostimen Microsoft Azure Active Directory (Azure AD) -suojausryhmä ei näy vaihtoehtona, kun luot sähköisen kaupankäynnin komponentteja Microsoft Dynamics Lifecycle Servicesissä (LCS) uuden sähköisen kaupankäynnin vuokraajan ensimmäisen käyttöönoton yhteydessä.

## <a name="description"></a>kuvaus

Kun luot sähköisen kaupankäynnin komponentit osana uutta sähköisen kaupankäynnin vuokraajaa, joka sisältää Commerce-sivuston luontiohjelman komponentin, Azure AD -suojausryhmä ei näy valintaikkunassa vaihtoehtona.

## <a name="resolution"></a>Ratkaisu

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>Sähköisen kaupankäynnin valmistelu käyttäjälle oikeassa vuokraajassa

1. Siirry [Azure-portaaliin](https://portal.azure.com/).
1. Noudata [Luo perusryhmä ja lisää jäsenet Azure Active Directoryn avulla](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal) -ohjeita siinä vuokraajassa, jolle sähköisen kaupankäynnin sivuston LCS-projekti valmisteltiin.
1. Siirry [LCS](https://lcs.dynamics.com/)-palveluun ja kirjaudu sisään käyttäen tiliä, jossa on sama vuokraaja kuin juuri luomallasi Azure AD -suojausryhmällä. Tilin on oltava käyttöoikeus, jotta se voi tarkastella Azure AD -suojausryhmää.
1. Konfiguroi sähköisen kaupankäynnin sivusto suorittamalla määritysvaiheet. Kun olet valmistellut sähköisen kaupankäynnin komponentit, suojausryhmän pitäisi nyt näkyä valintaikkunan vaihtoehtona.

> [!NOTE]
> Jotta voit varmistaa, että valintaikkunan kenttään tulee suojausryhmien luettelo, paina **Enter** sen jälkeen, kun olet kirjoittanut luomasi Azure AD- suojausryhmän nimen. Hakutulokset luetteloivat kaikki hakutekstillä alkavat Azure AD -suojausryhmät, joihin käyttäjällä on käyttöoikeus. Voit käyttää lyhyempää hakutermiä, kun haluat sallia laajemmat hakutulokset.

## <a name="additional-resources"></a>Lisäresurssit

[Perusryhmän luominen ja jäsenten Azure Active Directoryn avulla](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto](../deploy-ecommerce-site.md)