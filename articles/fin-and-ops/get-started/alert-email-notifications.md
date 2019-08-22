---
title: Asiakasohjelman hälytysilmoitukset sähköpostitse
description: Tässä ohjeaiheessa käsitellään sellaisten sääntöjen määrittämistä, jolla lähetetään sähköposti-ilmoituksia ennaltamääritettyjen tapahtumien sattuessa.
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 2f2db19316a999f804368ad60c5a6d1ead679f9f
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851020"
---
# <a name="client-alert-notifications-by-email"></a>Asiakasohjelman hälytysilmoitukset sähköpostitse

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Voit määrittää Microsoft Dynamics 365 for Finance and Operationsissa mukautetut hälytyssäännöt, jotka seuraavat tietojen suodatettuja näkyviä ja lähettävät automaattisesti sähköposti-ilmoituksia, kun ennaltamääritetyt tapahtumat tapahtuvat. Sähköposti-ilmoitusten lähetysasetus on käytettävissä kaikissa tuetuissa hälytystyypeissä, ja se voidaan käyttöön myös aiemmin luoduille hälytyssäännöille.

Voit käyttää valmiita ohjausobjektia ja luoda niiden avulla järjestelmän erätöiden suodatusnäkyviä seuraavia hälytyssääntöjä. **Tila**-kentän arvoa seuraamalla on mahdollista määrittää hälytyssääntöjä, jotka lähettävät sähköpostin, kun erätyö epäonnistuu. Näiden hälytyssääntöjen luonnin jälkeen sinun ei enää tarvitse tarkistaa liiketoimintatietojen muutoksia raporteista. Finance and Operationsin älykäs palvelu nimittäin havaitsee nämä muutokset ja seuraa niitä puolestasi.

Asiakasohjelman hälytykset määräytyvät Microsoft Office -integroinnin kautta saatavasta sähköpostin alijärjestelmästä. Suosituksena on SMTP (Simple Mail Transfer Protocol) -palvelun käyttö, jotta sähköpostin jakelu ei perustu paikalliseen sähköpostiohjelmaan.

Sähköpostitse lähetettävät ilmoitukset edellyttävät, että asiakkaat määrittävät integroidut sähköpostipalvelut. Sähköposti-ilmoitukset lähetetään vastaanottajille hälytyksen omistajien puolesta.

Lisätietoja sähköpostin määrittämisestä Finance and Operationsissa on kohdassa [Sähköpostiviestin määrittäminen ja lähettäminen](../organization-administration/configure-email.md).

Seuraavassa kuvassa on **Luo hälytyssääntö** -valintaikkuna, jossa on nyt myös **Lähetä sähköposti** -asetus.

[![Luo hälytyssääntö -valintaikkuna, jos Lähetä sähköposti -asetukseksi on valittu Kyllä](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Kun **Lähetä sähköposti** -asetukseksi on valittu **Kyllä**, hälytysilmoitusten toimittamista jatketaan toimintokeskuksesta.

## <a name="alert-notification-email-templates"></a>Hälytysilmoitusten sähköpostimallit

Palvelu lähettää sähköposti-ilmoituksia käyttämällä valmiita sähköpostimalleja, jotka toimittavat hälytysilmoituksen perustiedot.

Seuraavassa kuvassa on sähköpostitse toimitettujen hälytysilmoitusten rakenne.

[![Tietueen luontia, kentän muutoksia ja mallin poistoa koskevat mallipohjaiset hälytysilmoitukset](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)
