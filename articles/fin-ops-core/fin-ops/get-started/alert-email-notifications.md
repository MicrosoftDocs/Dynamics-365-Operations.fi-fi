---
title: Asiakasohjelman hälytysilmoitukset sähköpostitse
description: Tässä artikkelissa käsitellään sellaisten sääntöjen määrittämistä, jolla lähetetään sähköposti-ilmoituksia ennalta määritettyjen tapahtumien sattuessa.
author: RichdiMSFT
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 469c7fdda40780d6e559819103d73d7a4e7132a1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878275"
---
# <a name="client-alert-notifications-by-email"></a>Asiakasohjelman hälytysilmoitukset sähköpostitse

[!include [banner](../includes/banner.md)]

Voit määrittää mukautetut hälytyssäännöt, jotka seuraavat tietojen suodatettuja näkymiä ja lähettävät automaattisesti sähköposti-ilmoituksia, kun ennaltamääritetyt tapahtumat tapahtuvat. Sähköposti-ilmoitusten lähetysasetus on käytettävissä kaikissa tuetuissa hälytystyypeissä, ja se voidaan käyttöön myös aiemmin luoduille hälytyssäännöille.

Voit käyttää valmiita ohjausobjektia ja luoda niiden avulla järjestelmän erätöiden suodatusnäkyviä seuraavia hälytyssääntöjä. **Tila**-kentän arvoa seuraamalla on mahdollista määrittää hälytyssääntöjä, jotka lähettävät sähköpostin, kun erätyö epäonnistuu. Näiden hälytyssääntöjen luonnin jälkeen, liiketoimintatietojen muutoksia ei enää tarvitse tarkistaa raporteista. Älykäs muutoksen havaintopalvelu voi seurata näitä muutoksia puolestasi.

Asiakasohjelman hälytykset määräytyvät Microsoft Office -integroinnin kautta saatavasta sähköpostin alijärjestelmästä. Suosituksena on SMTP (Simple Mail Transfer Protocol) -palvelun käyttö, jotta sähköpostin jakelu ei perustu paikalliseen sähköpostiohjelmaan.

Sähköpostitse lähetettävät ilmoitukset edellyttävät, että asiakkaat määrittävät integroidut sähköpostipalvelut. Sähköposti-ilmoitukset lähetetään vastaanottajille hälytyksen omistajien puolesta.

Lisätietoja sähköpostin määrittämisestä on kohdassa [Sähköpostiviestin määrittäminen ja lähettäminen](../organization-administration/configure-email.md).

Seuraavassa kuvassa on **Luo hälytyssääntö** -valintaikkuna, jossa on nyt myös **Lähetä sähköposti** -asetus.

[![Luo hälytyssääntö -valintaikkuna, jos Lähetä sähköposti -asetukseksi on valittu Kyllä.](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Kun **Lähetä sähköposti** -asetukseksi on valittu **Kyllä**, hälytysilmoitusten toimittamista jatketaan toimintokeskuksesta.

## <a name="alert-notification-email-templates"></a>Hälytysilmoitusten sähköpostimallit

Palvelu lähettää sähköposti-ilmoituksia käyttämällä valmiita sähköpostimalleja, jotka toimittavat hälytysilmoituksen perustiedot.

Seuraavassa kuvassa on sähköpostitse toimitettujen hälytysilmoitusten rakenne.

[![Tietueen luontia, kentän muutoksia ja mallin poistoa koskevat mallipohjaiset hälytysilmoitukset.](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]