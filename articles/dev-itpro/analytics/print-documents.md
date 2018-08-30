---
title: Asiakirjan tulostus
description: "Voit tulostaa asiakirjat Microsoft Dynamics 365 for Finance and Operationsissa joko paikallisessa tulostimessa tai verkkotulostimessa. Tässä artikkelissa yhteenveto asiakirjojen tulostamisesta."
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro, Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 5d52568ce49b85f6215ed2835a95e2e016c9c879
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="document-printing"></a>Asiakirjan tulostus

[!include [banner](../includes/banner.md)]

Voit tulostaa asiakirjat Microsoft Dynamics 365 for Finance and Operationsissa joko paikallisessa tulostimessa tai verkkotulostimessa. Tässä artikkelissa yhteenveto asiakirjojen tulostamisesta.

<a name="printing-overview"></a>Tulostamisen yhteenveto
-----------------

Microsoft Dynamics 365 for Finance and Operationsissa on integroituja huolto- ja asiakasohjelmasovelluksia, joilla on helppo luoda, tallentaa ja jakaa liiketoimintoja tukevia asiakirjoja. Voit tulostaa asiakirjat Finance and Operationsissa joko paikallisessa tulostimessa tai verkkotulostimessa. Voit lisäksi viedä Finance and Operationsin sivuja ja raportteja suodaan asiakasohjelmista esimerkiksi PDF- tai Microsoft Office -tiedostoina. Ja koska työkuorma jaetaan, voi tulostaa liiketoiminta-asiakirjoja suoraan mobiililaitteesta verkkoresurssien avulla. Vaikka tulostusvaatimukset voivat vaihdella, kaikilla toimialoilla liiketoiminta-asiakirjat on yleensä tulostettava Finance and Operationsin avulla. Asiakirjojen tulostaminen verkkolaitteilla isännöidyistä sovelluksista tuo mukanaan aivan omanlaisensa haasteet. Seuraavassa on muutamia esimerkkejä:

-   Tulostimen ohjaimet eivät ehkä ole käytettävissä käyttäjän laitteessa.
-   Käyttäjän laitetta ei ole ehkä liitetty yritysverkkoon.

Kun järjestelmänvalvojat käyttävät tarkoitukseen varattua isäntään ja toimivat seuraavien helppojen ohjeiden mukaisesti, he voivat määrittää käyttöönotot siten, että käyttäjät voivat tulostaa suoraan verkkolaitteiden yrityssovelluksista.

### <a name="printing-scenarios-in-finance-and-operations-applications"></a>Finance and Operations -sovellusten tulostusskenaariot

Seuraavassa taulukossa on kolme keskeisintä Finance and Operations -sovellusten tulostusskenaariota.

| Skenaario                        | Tavoite                                                      | Ratkaisu                                                                                                            |
|---------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 1. Näkyvissä olevan tulostaminen        | Tulosta selaimessa näkyvä sisältö.             | Selaimeen muodostetaan verkkosivun tulostettava versio.                                             |
| 2. Vuorovaikutteinen tulostus         | Tulosta tietty asiakirja paikallisesti liitetyssä laitteessa. | Voit viedä raportin PDF-version ja ladata sen selaimeen.                                          |
| 3. Tulosta verkkolaitteessa | Lähetä tietty asiakirja toimialueen tulostimeen.     | Tietty asiakirja lähetetään asiakkaan toimialueella isännöidyssä tulostimessa toimivaan asiakassovellukseen. |

Koska ratkaisu vaihtelee skenaarion mukaan Finance and Operations -sovelluksiin sisältyy palveluja ja työkaluja, joiden avulla käyttäjät saavuttavat tavoitteensa:

-   Selain tukee **skenaariota 1** hahmontamalla HTML5-asiakasohjelman.
-   **Skenaario 2** käyttää asiakassovellusta ja Microsoft Office 365 -palveluja.
-   **Skenaario 3** edellyttää asiakassovellusten ja Microsoft Azuressa isännöityjen palvelujen tukea.

Azure-tilauksessa käyttöönotetun ympäristön lisäksi Finance and Operations -sovellukset antavat asiakkaille integroidun, ensikäden Azure-sovelluksen, joka helpottaa asiakirjojen tulostusta toimialueella isännöidyissä laitteissa.

## <a name="service-overview"></a>Palvelujen yhteenveto
Verkkoon liitetyssä laitteessa tulostusta odottavat isännöityjen sovellusten tuottamat asiakirjat tallennetaan Azure Blob -säilöön. [Asiakirjareitityksen agentti](install-document-routing-agent.md) muodostaa turvallisen kanavan Azure-palveluihin Azure-todennuksen avulla. **Suoritusjärjestys**

1.  Microsoft SQL Server Reporting Services (SSRS) luo raportin, joka tallennetaan Azure Blob -säilöön. Liitetyt tulostinasetukset tallennetaan yhdessä asiakirjan kanssa.
2.  Asiakirjareitityksen agentti kyselee aktiivisia töitä Azuren palveluväylän jonosta.
3.  Asiakirjareitityksen agentti lataa asiakirjan, joka viedään taustatulostukseen verkkotulostimeen.

Asiakasohjelmaan perustuvan ratkaisun ansiosta asiakkaat voivat hallita tulostustarpeidensa laajuutta. Paljon tulostavat asiakkaat voivat asentaa useita asiakirjareitityksen agentteja, mikä mahdollistaa entistä useamman samanaikaisen tulostoiminnan suorittamisen. Toisille asiakkaalle puolestaan riittää vain muutama asiakirjareitityksen agentti oletettujen tulostustarpeiden käsittelemiseen.

### <a name="service-components-for-network-printing"></a>Verkkotulostuksen palveluosat

Seuraavassa kaaviossa on verkkotulostusta tukevat perusosat. [![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png) Huomaa, että yhteen tulostimeen voidaan rekisteröidä useita asiakirjareitityksen agentteja. Isännöity palvelu ratkaisee tulostinasetukset käyttämällä verkkopolkua, joka tunnistaa yksilöllisesti jokaisen verkkotulostimen. Tämän vuoksi myös sellainen tulostin, johon on rekisteröity useita asiakasohjelmia, näkyy yhtenä valintana Finance and Operations -sovellusten käytettävissä olevien tulostimien luettelossa.




