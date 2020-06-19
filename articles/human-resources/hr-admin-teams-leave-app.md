---
title: Teamsin Human Resources -sovellus
description: Tässä ohjeaiheessa käsitellään Microsoft Teamsin Microsoft Dynamics 365 Human Resources -sovellusta.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 36684710e39c27840cc4aaa259a85579104fd8d6
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431127"
---
# <a name="human-resources-app-in-teams"></a>Teamsin Human Resources -sovellus

[!include [banner](includes/preview-feature.md)]

Microsoft Teamsin Microsoft Dynamics 365 Human Resources -sovelluksen avulla työntekijät voivat tehdä nopeasti poissaolopyyntöjä ja tarkastella poissaolosaldonsa tietoja Microsoft Teamsissa. Työntekijät voivat pyytää tietoja botin avustuksella. **Poissaolo**-välilehdessä on lisätietoja.

![Human Resources Teamsin lomasovelluksen botti](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources Teamsin lomasovelluksen Poissaolo-välilehti](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>Asentaminen ja määrittäminen

Human Resources -sovellus löytyy Teams-kaupasta. Lisätietoja Teams-sovelluksen asentamisesta on kohdassa [Lomapyyntöjen hallinta Teamsissa](hr-teams-leave-app.md).

Lisätietoja sovellusten käyttöoikeuksien hallinnasta Teamsissa on kohdassa [Sovellusten käyttöoikeuskäytäntöjen hallinta Microsoft Teamsissa](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="known-issues"></a>Tunnetut ongelmat

| Otto | Tila |
| --- | --- |
| Virhe: ongelma etsittäessä ympäristöä, johon muodostetaan yhteyttä. | Tämä virhe saattaa tulla näyttöön, vaikka olisit varmistanut, että käyttäjä voi käyttää yhtä tai useampaa henkilöstöresurssiympäristöä. Lisäksi et ehkä näe kaikkia odottamiasi ympäristöjä. Ennen kuin korjaat tämän ongelman, poista käyttäjä ja tuo ne sitten uudelleen, jotta ongelma voidaan ratkaista. |
| Saldo on virheellinen, kun lähetetään tulevaisuudessa olevaa päivämäärää koskeva poissaolo. | Ennakointi ei ole vielä käytettävissä. Saldo näkyy kuluvalta päivältä. |
| Kun aiemmin luodussa pyynnössä olevien tuntien määrää vähennetään, **Jäljellä jäävä saldo** pienenee eikä suurene. | Tämä tunnettu ongelma otetaan huomioon tulevaisuudessa. Näyttö on virheellinen, mutta summat oikaistaan lähetyksen yhteydessä. |
| Samoille päivämäärille näkyy kaksi **Tuleva poissaolo** -korttia. | Kortit ilmaisevat yksittäiset lähetykset. Palautetta otetaan edelleen vastaan ja muutoksia tehdään. |
| **Tarkistuksessa**-tilassa olevaa pyyntöä ei voi peruuttaa. | Tätä toimintoa ei tällä hetkellä tueta ja se lisätään tulevaan julkaisuun. |
| Saldotiedot lasketaan kuluvasta päivästä alkaen. | Järjestelmä ei tällä hetkellä näytä jaksotuskauden saldoa, vaikka se on määritetty loma- ja poissaoloparametreissa. |

## <a name="privacy-notice"></a>Tietosuojatiedot

Microsoft Teamsin Dynamics 365 Human Resources -botin avulla käyttäjän tekstinsyöttö analysoidaan, jotta taustalla oleva kysely tai tarkoitus saataisiin selville. Käyttäjän teksti, kuten Hae tili Contoso, reititetään yhteen Microsoftin kognitiiviseen palveluun, jonka nimi on Language Understanding Intelligent Service (LUIS). Lisätietoja LUIS-palvelusta on  [täällä](https://www.luis.ai/). LUIS-palvelu tulkitsee tai selvittää käyttäjän syötteen tarkoituksen (tässä tapauksessa tarkoituksena on etsiä tietoja) ja kohde-entiteetin (tässä tapauksessa tarkoitettu entiteetti on Contoso-niminen tili). Nämä tiedot välitetään sitten Microsoftin [Azure-bottikehykseen](https://azure.microsoft.com/services/bot-service/) , joka käyttää Dynamics 365 Human Resourcesin tietoja ja noutaa käyttäjän kyselyn haluamat tiedot. 

Asentamalla botin ja sallimalla sen käytön hyväksyt sen, että LUIS-palvelu ja Azure-bottikehys käsittelevät syötteen varsinaisen tarkoituksen, mikä parantaa käyttäjän keskustelukokemusta. LUIS-palvelun ja Azure-bottikehyksen vaatimustenmukaisuustasot voivat vaihdella Dynamics 365 Human Resourcesiin verrattuna. Vaikka LUIS-palvelu voi käyttää vain käyttäjäkyselyitä eikä sitä ole suunniteltu muodostamaan yhteyttä käyttäjän Dynamics 365 Human Resources -tietoihin tai -tiliin, Dynamics 365 Human Resources -botin käyttäjä voi vapaaehtoisesti tehdä kyselyn, joka sisältää asiakastietoja, henkilökohtaisia tietoja tai muita vastaavia tietoja ja kyseinen kysely voi tulla lähetetyksi LUIS-palveluun ja Azure-bottikehykseen. 

Käyttäjän kyselyjen ja viestien sisältöä säilytetään LUIS-järjestelmässä enintään 30 päivää. Nämä tiedot salataan eikä niitä käytetä koulutuksen tai palvelun parantamiseen. Lisätietoja kognitiivisista palveluista on  [täällä](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Microsoft Teamsin sovellusten järjestelmänvalvojan asetuksia hallitaan [Microsoft Teams -hallintakeskuksessa](https://admin.teams.microsoft.com/). 

## <a name="see-also"></a>Lisätietoja 

[Microsoft Teamsin lataaminen ja asentaminen](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teamsin ohje- ja tukikeskus](https://support.office.com/teams)</br>
[Loma- ja poissaolopyyntöjen hallinta Teamsissa](hr-teams-leave-app.md)

