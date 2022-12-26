---
title: Ei käytettävissä olevasta varastosta tai päivitysristiriidoista johtuvat laskelman kirjausvirheet
description: Tässä artikkelissa käsitellään varastoon liittyvien ongelmien kiertoteistä kirjattaessa laskelmaa Microsoft Dynamics 365 Commerceen.
author: Shajain
ms.date: 12/19/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: cebb890b42def6e9b002b01be63266b88bfc35a4
ms.sourcegitcommit: 4ad87483ba0bfea3e04fdb7e578d8abc34e607a4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2022
ms.locfileid: "9887626"
---
# <a name="statement-posting-errors-due-to-unavailable-inventory-or-update-conflicts"></a>Ei käytettävissä olevasta varastosta tai päivitysristiriidoista johtuvat laskelman kirjausvirheet

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa käsitellään varastoon liittyvien ongelmien kiertoteistä kirjattaessa laskelmaa Microsoft Dynamics 365 Commerceen.

## <a name="description"></a>kuvaus

Commerce-tapahtumien kirjausten aikana voidaan esiintyä virhesanomia, jotka liittyvät varasto-ongelmiin tai päivitysristiriitoihin.

### <a name="inventory-issues-error-message"></a>Varasto-ongelmien virhesanoma

Varasto-ongelmiin liittyvät virhesanomat voivat olla seuraavanlaisia:

> xx ei ole keräiltävissä, koska varastossa on vain yy käytettävissä

### <a name="update-conflict-error-messages"></a>Päivitysristiriitojen virhesanomat

Päivitysristiriita voi tapahtua, kun varaston arvostusmenetelmä on joko *standardikustannus* tai *liukuva keskiarvo*. Koska nämä molemmat menetelmät ovat jatkuvia kustannuslaskentamenetelmiä, lopullinen kustannus määräytyy kirjausajankohtana.

Jos käytössä on *Liukuva keskiarvo* -menetelmä, päivitysristiriidan virhesanoma on seuraavanlainen:

> Varaston arvoa xx.xx ei odoteta suhteellisen kululaskelman jälkeen

Jos käytössä on *Standardikustannus*-menetelmä, päivitysristiriidan virhesanoma on seuraavanlainen:

> Standardikustannus ei vastaa kirjanpitovaraston arvoa päivityksen jälkeen. Arvo = xx.xx, Määrä = yy.yy, Vakiokustannus = zz.zz

## <a name="resolutions"></a>Ratkaisut

### <a name="workaround-for-the-inventory-error"></a>Varastovirheen kiertäminen

Varastovirheen voi selvittää joko manuaalisesti päivittämällä nimikkeen varasto tai ottamalla käyttöön sen nimikemalliryhmän negatiivinen varasto, joka on liitetty varastoon Commerce headquartersissa.

Yhdenmukaisen kirjauskokemuksen luomiseksi Microsoft suosittelee, että negatiivisen fyysinen varasto otetaan käyttöön nimikemalliryhmässä. Joissakin tilanteissa laskelmia ei ehkä voi kirjata, ellei negatiivista fyysistä varastoa ole otettu käyttöön.

Esimerkki: Nimikettä ei ole saatavana varastossa mutta kassa palauttaa nimikkeen ja lisää sen sitten takaisin samaan tapahtumaan alennettuun hintaan, mikä imitoi hintavastaavuuden. Tässä tapauksessa sekä palautustapahtuma että myyntitapahtuma viedään samaan yhden asiakastilauksen laskelmaan. Koska kuitenkaan ei voida taata, että palautusrivi (joka kasvattaa varastoa) kirjataan ennen myyntirivin (joka vähentää varastoa) kirjausta, varastovirheitä voi tapahtua. Jos negatiivinen fyysinen varasto on otettu käyttöön tässä tilanteessa, tapahtuman kirjaus ei vaikuta negatiivisesti ja järjestelmä näyttää varaston oikein.

#### <a name="enable-negative-physical-inventory-for-an-item-model-group"></a>Negatiivisen fyysisen varaston ottaminen käyttöön nimikemalliryhmässä

Nimikemalliryhmän negatiivinen fyysinen varasto otetaan käyttöön Commerce headquartersissa seuraavasti.

1. Valitse **Varastonhallinta \> Asetukset \> Varasto**.
1. Valitse vasemmassa siirtymisruudussa nimikemalliryhmä.
1. Valitse **Varastokäytännöt**-osan **Negatiivinen varasto** -kohdassa **Fyysinen negatiivinen varasto** -valintaruutu.

![Fyysinen negatiivinen varasto on otettu käyttöön](./media/Physical_Negative_Inventory.png)

### <a name="workaround-for-the-update-conflict-error"></a>Päivitysristiriitavirheen kiertäminen

Lisätietoja päivitysristiriitavirheen mahdollisista korjaustavoista on kohdassa [Päivitysristiriita tapahtuu, kun varaston arvostusmenetelmä on joko standardikustannus tai liukuva keskiarvo](/troubleshoot/dynamics-365/supply-chain/costing/update-conflict-standard-cost-moving-average-inventory-valuation).

> [!NOTE]
> Päivitysristiriitavirheen vuoksi ei tarvitse poistaa asiakastilauksia, jotka luotiin kirjauksen koostevaiheen avulla. Kun ehdotetut kiertotiet on korjaustavat on toteutettu, laskelman kirjaamisen pitäisi onnistua, kun sitä yritetään uudelleen.
