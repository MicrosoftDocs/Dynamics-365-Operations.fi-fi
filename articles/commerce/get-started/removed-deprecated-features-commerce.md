---
title: Poistetut tai vanhentuneet Dynamics 365 Commerce -ominaisuudet
description: Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Commercesta.
author: josaw
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: aa18e7446a72a907fcad70f92ea529088b6cecbd
ms.sourcegitcommit: 83c7e5ab54c1cad2e21e33769cc524cfa4213f58
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/07/2020
ms.locfileid: "3539876"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Poistetut tai vanhentuneet Dynamics 365 Commerce -ominaisuudet

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Commercesta.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi. 

> [!NOTE]
> Seuraavissa raporteissa on tarkempia tietoja Finance and Operations -sovellusten objekteista: [Teknisten tietojen raportit](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Voit verrata raporttien eri versioita saadaksesi lisätietoja objekteista, jotka on muutettu tai poistettu kussakin Finance and Operations -sovelluksissa.

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Commercen version 10.0.11 poistetut tai vanhentuneet ominaisuudet
### <a name="data-action-hooks"></a>Tietotoiminnon koukut
|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tietotoiminnon koukkutoiminto on vanhentunut suorituskykyongelmien vuoksi. |
| **Onko toinen ominaisuus korvannut?**   | Liiketoimintalogiikkaa kannattaa muokata tietotoimintokerroksessa [tietotoiminnon ohitusten](../e-commerce-extensibility/data-action-overrides.md) avulla.|
| **Tuotealueet, joihin vaikutetaan**         | Sähköisen kaupankäynnin laajennettavuuden tietotoiminnot |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: versiosta 10.0.11 alkaen |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Visual Studio 2015:n Retail SDK -tuki, msbuild 14.0 ja Retail SDK\Viitekirjastot ja työkalut
|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Visual Studio 2015:n Retail SDK -tuki on vanhentunut, ja se on päivitetty tukemaan versiota VS 2017, msbuild 15.0 sekä kaikki viitekirjastot ja kaupankäynnin välityspalvelimen luontityökalut RetailSDK\References-kansiossa siirrettiin NuGet-paketteihin yksinkertaistamaan laajennusmallia ja SDK-päivitysprosessia.|
| **Onko toinen ominaisuus korvannut?**   | Järjestelmä kannattaa päivittää kohdan [Retail SDK:n siirtäminen Visual Studio 2015:sta Visual Studio 2017:ään](../dev-itpro/retail-sdk/migrate-sdk.md) ohjeiden mukaisesti. |
| **Tuotealueet, joihin vaikutetaan**         | Retail SDK -laajennukset |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: versiosta 10.0.11 alkaen |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>Retail Server -laajennuksessa käytössä IEdmModelExtender ja CommerceController
|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Retail Server -laajennus, jossa on käytössä IEdmModelExtender ja CommerceController, on vanhentunut, jotta yksinkertaistettu laajennusmalli on mahdollinen. Uudessa toteutuksessa on vain ohjainluokka ilman ylimääräistä IEdmModelExtender-luokan toteutusta. Tällä tavoin vältetään myös riippuvuus tietystä OData-versiosta (jos OData-version päivitetään, laajennukset voivat vaurioitua). |
| **Onko toinen ominaisuus korvannut?**   |  IController-luokan laajennusmallia kannattaa käyttää tuomalla NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) -paketti. |
| **Tuotealueet, joihin vaikutetaan**         | Retail Serverin laajennukset |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: versiosta 10.0.11 alkaen |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Laiteasemalaajennus IHardwareStationControllerin avulla
|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | IHardwareStationControlleria käyttävä laiteasemalaajennus on vanhentunut, jotta yksinkertaistettu laajennusmalli on mahdollinen. Uudessa toteutuksessa on vain IController-luokka ilman lisäluokkien toteutuksia, jolloin ei myöskään synny riippuvuutta peruslaiteasemakirjastoista, kun aiemmin laajennuksen oli viitattava useisiin kirjastoihin.) |
| **Onko toinen ominaisuus korvannut?**   | IController-luokan laajennusmallia kannattaa käyttää tuomalla NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) -paketti. |
| **Tuotealueet, joihin vaikutetaan**         | Laiteasemalaajennukset |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: versiosta 10.0.11 alkaen |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Commercen version 10.0.10 poistetut tai vanhentuneet ominaisuudet
### <a name="pos-operation-803---picking-and-receiving"></a>Myyntipistetoiminto 803 - Keräys ja vastaanotto
|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Keräilyn ja vastaanoton toimintoja ollaan poistamassa, koska uusi uudelleensuunnittelu on käytössä. |
| **Onko toinen ominaisuus korvannut?**   | Kyllä. Se korvataan kahdella uudella myyntipistetoiminnolla: saapuva työvaihe (804) ja lähtevä työvaihe (805).|
| **Tuotealueet, joihin vaikutetaan**         | Myyntipiste (POS) -sovellus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: kun kyseessä on julkaisuversio 10.0.10, keräily- ja vastaanottotoiminto ei enää vastaanota uusia ominaisuuspäivityksiä. Vain kriittiset ohjelmakorjaukset tehdään tämän toiminnon yhteydessä tulevissa versioissa. Kaikkia asiakkaita kannustetaan siirtymään uusiin [saapuviin työvaiheisiin](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) ja [lähteviin toimintoihin](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), jotka ovat jatkossakin osa pitkän aikavälin tuotesuunnitelmaa. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Commercen version 10.0.7 poistetut tai vanhentuneet ominaisuudet
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities- ja GetAvailableInventoryNearby ohjelmointirajapintaliittymät
|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Uudet optimoidut ohjelmointirajapinnat on luotu korvaamaan GetProductAvailabilities- ja GetAvailableInventoryNearby-ohjelmointirajapinnat. |
| **Onko toinen ominaisuus korvannut?**   | Kyllä: sen tilalle tulee GetEstimatedAvailabilty ja GetEstimatedProductWarehouseAvailability -ohjelmointirajapinnat. |
| **Tuotealueet, joihin vaikutetaan**         | e-Commerce-sovellus-SDK |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: Julkaisuversiosta 10.0.7 alkaen kohteille GetProductAvailabilities ja GetAvailableInventoryNearby ei tehdä enää teknisiä investointeja. Organisaatiot, jotka käyttävät näitä ohjelmointirajapintaliittymiä verkkokaupan käyttöönotoissa, on muunnettava uuteen GetEstimatedAvailabilty- ja GetEstimatedProductWarehouseAvailability-ohjelmointirajapintaliittymiin ja otettava käyttöön [Optimoitu tuotteen saatavuuden laskentaominaisuus](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Poistettujen tai vanhentuneiden toimintojen aiemmat ilmoitukset
Lisätietoja poistetuista tai vanhentuneista toiminnoista aiemmissa versioissa on kohdassa [Poistetut tai vanhentuneet toiminnot edellisissä versioissa](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).
