---
title: Asiakasohjelman hälytysilmoitukset sähköpostitse
description: Tässä ohjeaiheessa käsitellään sellaisten sääntöjen määrittämistä, jolla lähetetään sähköposti-ilmoituksia ennaltamääritettyjen tapahtumien sattuessa.
author: tjvass
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: fe422d645c8f2c0c564af30624090828e10ea4bf
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567249"
---
# <a name="client-alert-notifications-by-email"></a>Asiakasohjelman hälytysilmoitukset sähköpostitse

[!include [banner](../includes/banner.md)]

Voit määrittää mukautetut hälytyssäännöt, jotka seuraavat tietojen suodatettuja näkymiä ja lähettävät automaattisesti sähköposti-ilmoituksia, kun ennaltamääritetyt tapahtumat tapahtuvat. Sähköposti-ilmoitusten lähetysasetus on käytettävissä kaikissa tuetuissa hälytystyypeissä, ja se voidaan käyttöön myös aiemmin luoduille hälytyssäännöille.

Voit käyttää valmiita ohjausobjektia ja luoda niiden avulla järjestelmän erätöiden suodatusnäkyviä seuraavia hälytyssääntöjä. **Tila**-kentän arvoa seuraamalla on mahdollista määrittää hälytyssääntöjä, jotka lähettävät sähköpostin, kun erätyö epäonnistuu. Näiden hälytyssääntöjen luonnin jälkeen, liiketoimintatietojen muutoksia ei enää tarvitse tarkistaa raporteista. Älykäs muutoksen havaintopalvelu voi seurata näitä muutoksia puolestasi.

Asiakasohjelman hälytykset määräytyvät Microsoft Office -integroinnin kautta saatavasta sähköpostin alijärjestelmästä. Suosituksena on SMTP (Simple Mail Transfer Protocol) -palvelun käyttö, jotta sähköpostin jakelu ei perustu paikalliseen sähköpostiohjelmaan.

Sähköpostitse lähetettävät ilmoitukset edellyttävät, että asiakkaat määrittävät integroidut sähköpostipalvelut. Sähköposti-ilmoitukset lähetetään vastaanottajille hälytyksen omistajien puolesta.

Lisätietoja sähköpostin määrittämisestä on kohdassa [Sähköpostiviestin määrittäminen ja lähettäminen](../organization-administration/configure-email.md).

Seuraavassa kuvassa on **Luo hälytyssääntö** -valintaikkuna, jossa on nyt myös **Lähetä sähköposti** -asetus.

[![Luo hälytyssääntö -valintaikkuna, jos Lähetä sähköposti -asetukseksi on valittu Kyllä](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Kun **Lähetä sähköposti** -asetukseksi on valittu **Kyllä**, hälytysilmoitusten toimittamista jatketaan toimintokeskuksesta.

## <a name="alert-notification-email-templates"></a>Hälytysilmoitusten sähköpostimallit

Palvelu lähettää sähköposti-ilmoituksia käyttämällä valmiita sähköpostimalleja, jotka toimittavat hälytysilmoituksen perustiedot.

Seuraavassa kuvassa on sähköpostitse toimitettujen hälytysilmoitusten rakenne.

[![Tietueen luontia, kentän muutoksia ja mallin poistoa koskevat mallipohjaiset hälytysilmoitukset](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]