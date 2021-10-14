---
title: Ylläpidä tuotemääritysmallin tuoterakennetta
description: Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd78b06f10d0c9b1df57dacdd824b06ebe414b3b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577285"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Ylläpidä tuotemääritysmallin tuoterakennetta

[!include [banner](../../includes/banner.md)]

Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin. Tämä menettely luodaan käyttämällä USMF-demoyrityksen Korkealaatuinen kaiutin -mallia.

## <a name="add-a-bom-line"></a>Lisää tuoterakennerivi

1. Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotekonfiguraation mallit**.
1. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse tähän menettelyyn korkealaatuinen kaiutin.  
1. Valitse luettelossa valitulla rivillä oleva linkki.
1. Laajenna **Tuoterakennerivi**-osa.
1. Valitse **Lisää**.
1. Kirjoita arvo **Nimi**-kenttään.
1. Kirjoita **Kuvaus**-kenttään arvo.
1. Valitse **Tallenna**.

## <a name="add-bom-line-details"></a>Lisää tuoterakennerivin tiedot

1. Valitse **Tuoterakennerivin tiedot**.
2. Syötä tai valitse arvo **Nimiketunnus**-kentässä.
    * Valitse esimerkiksi nimike M0055.  
    * Voit valita kunkin tuoterakennerivin ominaisuuden kohdalla, annetaanko sille kiinteä arvo vai yhdistetäänkö se määritteeseen.  
3. Valitse **Määritä**-valintaruutu.
4. Valitse **Laskenta**-kentässä *Kyllä*.
    * **Laskelma**-ominaisuuden määrittäminen arvoksi *Kyllä* varmistaa, että tuoterakennerivi sisältyy kustannuslaskentaan.  
5. Valitse **Määritys**-välilehti.
6. Valitse **Määritä**-valintaruutu.
7. Anna **Määrä**-kentässä numero.
    * Määräkenttä määrittää, miten suuri osa nimikkeestä sisällytetään tuoterakenteeseen. Tämä voisi olla hyvä ehdokas määritteen yhdistämiselle.  
8. Valitse **Dimensio**-välilehti.
    * Tarkista, onko yksikään tuotedimensio aktiviinen ja onko sillä siksi oltava arvo tai määrite määritettynä.  
9. Valitse **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]