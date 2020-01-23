---
title: Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (11. tammikuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d49a4aca368e3de10ae37b56c6d286d78f7f369a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899171"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-11-2019"></a>Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (11. tammikuuta 2019)

**Koontiversio 8.1.2100**

Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.

## <a name="changes"></a>Muutokset

### <a name="validate-leave-requests-by-forecasting-available-balance"></a>Lomapyyntöjen vahvistaminen ennakoimalla käytettävissä oleva saldo
Tähän versioon tehtyjen muutosten ansiosta työntekijät voivat tehdä lomapyynnön ilman, että se vähennetään heidän nykyisestä saldostaan. Tulevaisuuteen sijoittuvissa pyynnöissä käytetään vakiotyönkulkua. Lisätietoja on kohdassa [Jaksotettu poissaolo tehtyjen työtuntien mukaan](leave-accrue-hours-worked.md).

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a>Ennakoidun lomasaldon näyttäminen ESS- ja Henkilöt-työtiloissa
Tämän ominaisuuden ansiosta henkilöstöosasto, esimiehet ja työntekijät voivat tarkastella tulevien lomajaksojen saldoja. Työntekijät voivat tarkastella tulevia saldoja **Työntekijän itsepalvelu** -työtilassa, kun taas henkilöstöosasto saa samat tiedot käyttöönsä **Ihmiset**-työtilassa.

### <a name="notifications-for-changing-leave-balances"></a>Lomasaldojen muutosilmoitukset
Lomasaldot näyttävät työntekijöiden nykyisen saldon. Tulevat saldot saadaan näkyviin **Työntekijän itsepalvelu**- ja **Henkilöt**-työtiloissa antamalla alkaen-päivämäärä, jonka perusteella ennakoitu saldo lasketaan.

Siirtyminen on lisätty seuraaville alueille ennakoitujen saldojen katsomista varten:
  - **Poissaoloaika**-kortti **Työntekijän itsepalvelu** -työtilassa.
  - **Loma ja poissaolo** -kortti **Esimiehen itsepalvelu** -työtilassa.
  - **Loma ja poissaolo**-sivu **Henkilöt**-työtilassa.

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a>Desimaalien salliminen muuttuvan kompensaation suunnitelmissa (käteissuunnitelmat)
Muuttuvat käteispalkkiot ja -suunnitelmat on nyt entistä joustavampia sellaisten summien ja ohitusten osalta, joiden arvoissa on desimaaleja.

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a>Muuttuvan kompensaation rekisteröintien päivämääriä ei voi muuttaa suunnitelman tallennuksen jälkeen
Tämän muutoksen ansiosta suunnitelma ja päivämäärä voidaan päivittää (pidennetty tai päätetty) suunnitelman tallennuksen jälkeen. Voit edelleen aktivoida suunnitelmat tai poistaa niiden aktivoinnin aloitus- ja päättymispäivämääristä riippumatta.

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a>Palkanlaskentatietojen käytettävissä määritetyn palkanlaskentakoordinaattorin käyttöoikeusroolin myötä
Palkanlaskentakoordinaattorin rooli on päivitetty antaa palkanlaskentatietojen käyttöoikeus pyyntöprosessin aikana.

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Työntekijän itsepalvelu | Toimihierarkiaan porautuminen ruudusta ei päädy pääsolmuun
Tehdyillä muutoksilla estetään virhe, joka esiintyi, kun toimihierarkia lisättiin uuteen työtilaan ja organisaatiohierarkiassa siirryttäessä.

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a>Uusi vahvistussanoma henkilöstönumerosarjaa käytettäessä
Tehty muutos selkeyttää, mistä ongelmasta oli kyse, kun palkkasit työntekijän ja käytössä on seuraava henkilöstönumero.

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a>Työntekijän itsepalvelu -työtila valittu alkuperäiseksi aloitussivuksi
Kun **Työntekijän itsepalvelu** -työtila on valittu käyttäjän alkuperäiseksi aloitussivuksi mutta kyseiselle käyttäjälle ei ole määritetty työntekijäroolia, järjestelmää ohjaa käyttäjän oletuskoontinäyttöön.

### <a name="termination-reason-code-updates-position-assignment-record"></a>Työsuhteen päättämisen syykoodi päivittää toimen määritystietueen
Työsuhteen päättämisen syykoodi päivittää nyt toimimäärityksen, kun työntekijän työsuhde päättyy ja toimi lopetetaan. 
