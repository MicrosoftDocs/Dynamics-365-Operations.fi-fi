---
title: Sähköisen laskutuksen lisäosan käytön aloittaminen
description: Tässä aiheessa on tietoja, joiden avulla voit aloittaa sähköisen laskutuksen lisäosan käytön Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.
author: gionoder
manager: AnnBe
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 07954c5c96f390bc651794f8b6c61f2a1a17ab8b
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111217"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Sähköisen laskutuksen lisäosan käytön aloittaminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa on tietoja, joiden avulla voit aloittaa sähköisen laskutuksen lisäosan käytön.

Seuraavassa taulukossa luetellaan sähköisen laskutuksen ominaisuudet ja liiketoimintaasiakirjat, joihin niitä voidaan käyttää.

| Toiminnon nimi                         | Yritysasiakirja |
|--------------------------------------|-------------------|
| Itävallan sähköiset laskut (AT)    | <p>Myyntilasku</p><p>Projektilasku</p> |
| Belgian sähköinen lasku (BE)      | <p>Myyntilasku</p><p>Projektilasku</p> |
| Brasilian NF-e (BR)                  | <p>Mallin 55 veroasiakirja</p><p>Oikaisukirje</p> |
| Brasilian NFS-e ABRASF Curitiba (BR) | Palvelun veroasiakirja |
| Brasilian NFS-e São Paulo (BR)       | Palvelun veroasiakirja |
| Tanskan sähköinen lasku (DK)       | <p>Myyntilasku</p><p>Projektilasku</p> |
| Egyptin sähköinen lasku (EG)     | <p>Myyntilasku</p><p>Projektilasku</p> |
| Viron sähköinen lasku (EE)     | <p>Myyntilasku</p><p>Projektilasku</p> |
| Suomen sähköinen lasku (FI)       | <p>Myyntilasku</p><p>Projektilasku</p> |
| Ranskan sähköinen lasku (FR)       | <p>Myyntilasku</p><p>Projektilasku</p> |
| Saksan sähköinen lasku (DE)       | <p>Myyntilasku</p><p>Projektilasku</p> |
| FatturaPA (IT)                       | <p>Myyntilasku</p><p>Projektilasku</p> |
| Meksikon CFDI Interfactura (MX)       | <p>Myyntilasku</p><p>Pakkausluettelo</p><p>Varastosiirto</p><p>Maksun täydennys</p> |
| Alankomaiden sähköinen lasku (NL)        | <p>Myyntilasku</p><p>Projektilasku</p> |
| Norjan sähköinen lasku (NO)    | <p>Myyntilasku</p><p>Projektilasku</p> |
| Espanjan sähköinen lasku (ES)      | <p>Myyntilasku</p><p>Projektilasku</p> |
| Sähköinen PEPPOL-lasku            | <p>Myyntilasku</p><p>Projektilasku</p> |

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit suorittaa tämän ohjeaiheen vaiheita, seuraavien edellytysten on toteuduttava:

- Konfiguroi Regulatory Configuration Service (RCS) ja Microsoft Dynamics 365 Finance- tai Dynamics 365 Supply Chain Management -ympäristösi niin, että voit lähettää sähköisen laskutuksen lisäosaan.
- Luo palveluympäristö ja julkaise se sähköisen laskutuksen lisäosaan. Lisätietoja on ohjeaiheessa [Sähköisen laskutuksen lisäpalvelun hallinnan käytön aloittaminen](e-invoicing-get-started-service-administration.md).
- Luo yhdistetty sovellus. Lisätietoja on ohjeaiheessa [Sähköisen laskutuksen lisäpalvelun hallinnan käytön aloittaminen](e-invoicing-get-started-service-administration.md).
- Luo organisaatiollesi konfiguraatiopalvelu. Lisätietoja on kohdassa [Määrityspalvelun luonti ja merkitseminen aktiiviseksi](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Tuo sähköisen laskutuksen ominaisuus Microsoftin konfiguraatiopalvelusta. 

1. Kirjaudu sisään Regulatory Configuration Service (RCS) -tilillesi.
2. Valitse **Globalisointitoiminnot**-työtila ja **Toiminnot**-kohdan **Sähköinen laskutus** -ruutu.
3. Valitse **Tuo** ja valitse sitten **Synkronoi**.
4. Suodata **Konfigurointipalvelu**-sarake hakusanan **Microsoft** avulla.
5. Valitse sähköisen laskutuksen toiminnon nimi tämän ohjeaiheen alussa olevasta taulusta ja valitse sitten **Tuo**.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Luo organisaation palveluntarjoajassa sähköisen laskutuksen ominaisuus

1. Valitse RCS:n **Globalisointitoiminnot**-työtilan **Toiminnot**-kohdassa **Sähköinen laskutus** -ruutu.
2. Valitse **Lisää** > **Perustuu aiempaan ominaisuuteen** ja anna **Nimi**-kentässä sähköisen lasktuksen ominaisuuden nimi.
3. Anna ominaisuuden kuvaus **Kuvaus**-kentässä.
4. Valitse **Perustoiminto**-kentästä tuotu sähköinen laskutusominaisuus Microsoftin konfiguraatiopalvelusta.
5. Valitse **Luo ominaisuus**.

## <a name="configure-the-electronic-invoicing-feature"></a>Konfiguroi sähköisen laskutuksen ominaisuus

Maan tai alueen mukaan sähköinen laskutustoiminto saattaa edellyttää lisäkonfiguraatiota. Yksityiskohtaiset vaiheet ovat maasi tai alueesi käytettävissä olenassa aloitusdokumentaatiossa.

## <a name="configure-the-application-setup"></a>Määritä sovellusasetukset

1. Valitse luomasi Sähköinen laskutus -toiminto.
2. Tarkista **Versio**-välilehdessä, että **Luonnos**-versio on valittuna.
3. Valitse **Asetukset** -välilehdessä **Sovelluksen asetukset**.

    > [!NOTE]
    > Tarkista, että organisaatiosi on määritetty **aktiiviseksi** konfiguraatiopalveluksi. Lisätietoja on kohdassa [Määrityspalvelun luonti ja merkitseminen aktiiviseksi.](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)

4. Valitse **Toiminnon määritys** ja sitten **Yhdistetty sovellus**.
5. Valitse **Sähköisen asiakirjan tyypit** -osassa **Lisää**.
6. Valitse ja määritä jokaiselle toiminnon tukemalle liiketoimintatiedostolle **Taulun nimi** -arvo seuraavan taulukon mukaisesti:

    | Toiminnon nimi                         | Yritysasiakirja | Taulun nimi |
    |--------------------------------------|-------------------|------------|
    | Itävallan sähköiset laskut (AT)    | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Belgian sähköinen lasku (BE)      | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Brasilian NF-e (BR)                  | <p>Veroasiakirja</p><p>Oikaisukirje</p> | Veroasiakirja |
    | Brasilian NFS-e ABRASF Curitiba (BR) | Palvelun veroasiakirja | Veroasiakirja |
    | Brasilian NFS-e São Paulo (BR)       | Palvelun veroasiakirja | Veroasiakirja |
    | Tanskan sähköinen lasku (DK)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Egyptin sähköinen lasku (EG)     | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Viron sähköinen lasku (EE)     | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Suomen sähköinen lasku (FI)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Ranskan sähköinen lasku (FR)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Saksan sähköinen lasku (DE)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | FatturaPA (IT)                       | <p>Myyntilasku</p><p>Projektilasku | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Meksikon CFDI Interfactura (MX)       | <p>Myyntilasku</p><p>Pakkausluettelo</p><p>Varastosiirto</p><p>Maksun täydennys</p> | Myyntilaskukirjauskansio |
    | Alankomaiden sähköinen lasku (NL)        | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Norjan sähköinen lasku (NO)    | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Espanjan sähköinen lasku (ES)      | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Sähköinen PEPPOL-lasku            | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |

7. Valitse ja määritä jokaiselle toiminnon tukemalle liiketoimintatiedostolle **Konteksti** -arvo seuraavan taulukon mukaisesti:

    | Toiminnon nimi                         | Yritysasiakirja | Konteksti |
    |--------------------------------------|-------------------|---------|
    | Itävallan sähköiset laskut (AT)    | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Belgian sähköinen lasku (BE)      | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Brasilian NF-e (BR)                  | <p>Veroasiakirja</p><p>Oikaisukirje</p> | <p>Myyntilaskun kontekstimalli – veroasiakirjan konteksti</p><p>Myyntilaskun kontekstimalli – veroasiakirjan oikaisukirjeen konteksti</p> |
    | Brasilian NFS-e ABRASF Curitiba (BR) | Palvelun veroasiakirja| Myyntilaskun kontekstimalli – veroasiakirjan konteksti |
    | Brasilian NFS-e São Paulo (BR)       | Palvelun veroasiakirja| Myyntilaskun kontekstimalli – veroasiakirjan konteksti |
    | Tanskan sähköinen lasku (DK)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Egyptin sähköinen lasku (EG)     | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Viron sähköinen lasku (EE)     | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Suomen sähköinen lasku (FI)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Ranskan sähköinen lasku (FR)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Saksan sähköinen lasku (DE)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | FatturaPA (IT)                       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Meksikon CFDI Interfactura (MX)       | <p>Myyntilasku</p><p>Pakkausluettelo</p><p>Varastosiirto</p><p>Maksun täydennys</p> | Myyntilaskun kontekstimalli – myyntilaskun konteksti |
    | Alankomaiden sähköinen lasku (NL)        | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Norjan sähköinen lasku (NO)    | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Espanjan sähköinen lasku (ES)      | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Sähköinen PEPPOL-lasku            | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |

8. Valitse ja määritä jokaiselle toiminnon tukemalle liiketoimintatiedostolle **Liiketoiminta-asiakirjan yhdistäminen** -arvo seuraavan taulukon mukaisesti:

    | Toiminnon nimi                         | Yritysasiakirja | Liiketoiminta-asiakirjan yhdistämismääritys |
    |--------------------------------------|-------------------|---------------------------|
    | Itävallan sähköiset laskut (AT)    | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Belgian sähköinen lasku (BE)      | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Brasilian NF-e (BR)                  | <p>Veroasiakirja</p><p>Oikaisukirje</p> | <p>Veroasiakirjan määritys – veroasiakirjan määritys</p><p>Veroasiakirjan määritys – oikaisukirjeen määritys</p> |
    | Brasilian NFS-e ABRASF Curitiba (BR) | Palvelun veroasiakirja | Veroasiakirjan määritys – veroasiakirjan määritys |
    | Brasilian NFS-e São Paulo (BR)       | Palvelun veroasiakirja | Veroasiakirjan määritys – veroasiakirjan määritys |
    | Tanskan sähköinen lasku (DK)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Egyptin sähköinen lasku (EG)     | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Viron sähköinen lasku (EE)     | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Suomen sähköinen lasku (FI)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Ranskan sähköinen lasku (FR)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Saksan sähköinen lasku (DE)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | FatturaPA (IT)                       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Meksikon CFDI Interfactura (MX)       | <p>Myyntilasku</p><p>Pakkausluettelo</p><p>Varastosiirto</p><p>Maksun täydennys</p> | Laskumallin määritys – Myyntilasku |
    | Alankomaiden sähköinen lasku (NL)        | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Norjan sähköinen lasku (NO)    | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Espanjan sähköinen lasku (ES)      | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Sähköinen PEPPOL-lasku            | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |

Maan tai alueen mukaan sähköinen laskutustoiminto saattaa edellyttää lisäkonfiguraatiota. Yksityiskohtaiset vaiheet ovat maasi tai alueesi käytettävissä olenassa aloitusdokumentaatiossa.

## <a name="deploy-the-electronic-invoicing-feature"></a>Ota sähköisen laskutuksen ominaisuus käyttöön

1. Valitse **Versiot**-välilehdestä se sähköisen laskutuksen toiminnon versio, jonka haluat ottaa käyttöön.
2. Valitse **Muutoksen tila** \> **Viimeistele**.
3. Valitse **Muuta tilaa** \> **Julkaise**.
4. Valitse **Ota käyttöön**.
5. Määritä **Ota käyttöön yhdistetyssä sovelluksessa** -asetuksen arvoksi **Kyllä**.
6. Valitse **Yhdistä sovellus** -sivulla yhteys, joka liittyy Financen tai Supply Chain Managementin esiintymään.
7. Määritä **Ota käyttöön palveluympäristössä** -asetuksen arvoksi **Kyllä**.
8. Valitse **Palveluympäristö**-kentästä sähköinen laskutuksen lisäpalvelun ympäristö, jossa haluat ottaa sähköisen laskutuksen ominaisuuden käyttöön.
9. Valitse **Päivämäärästä**-kentässä päivämäärä, jolloin sähköisen laskutuksen ominaisuuden tulee olla voimassa sähköisen laskutuksen lisäosassa.
10. Valitse **OK**.

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>Sähköisen laskutuksen ominaisuuden käyttöönotto Financessa tai Supply Chain Managementissa

1. Kirjaudu sisään Financeen tai Supply Chain Managementiin ja varmista, että olet oikeassa yrityksessä.
2. Siirry kohtaan **Organisaation hallinta** \> **Määritys** \> **Sähköisten asiakirjojen parametrit**.
3. Valitse **Ominaisuudet**-välilehdessä toimintoviite tai -viitteet, jotka on lueteltu seuraavassa taulukossa, kun haluat ottaa sähköisen laskutuksen käyttöön Financessa tai Supply Chain Managementissa.

    | Toiminnon nimi                         | Maa tai alue  | Ominaisuuden viite |
    |--------------------------------------|-----------------|-------------------|
    | Itävallan sähköiset laskut (AT)    | Itävalta         | EUR-00023 |
    | Belgian sähköinen lasku (BE)      | Belgia         | EUR-00023 |
    | Brasilian NF-e (BR)                  | Brasilia          | BR-00053 |
    | Brasilian NFS-e ABRASF Curitiba (BR) | Brasilia          | BR-00095 |
    | Brasilian NFS-e São Paulo (BR)       | Brasilia          | BR-00095 |
    | Tanskan sähköinen lasku (DK)       | Tanska         | <p>EUR-00023</p><p>DK-00001</p> |
    | Alankomaiden sähköinen lasku (NL)        | Alankomaat | EUR-00023 |
    | Egyptin sähköinen lasku (EG)     | Egypti           | EG-00008 |
    | Viron sähköinen lasku (EE)     | Viro         | EUR-00023 |
    | Suomen sähköinen lasku (FI)      | Suomi         | EUR-00023 |
     Ranskan sähköinen lasku (FR)       | Ranska           | EUR-00023 |
    | Saksan sähköinen lasku (DE)       | Saksa         | EUR-00023 |
    | Meksikon CFDI Interfactura (MX)       | Meksiko          | <p>MX-00010</p><p>MX-00016</p> |
    | Norjan sähköinen lasku (NO)    | Norja          | <p>EUR-00023</p><p>NO-00010</p> |
    | Espanjan sähköinen lasku (ES)      | Espanja           | <p>EUR-00023</p><p>ES-00025</p> |
    | Italian sähköinen lasku (IT)      | Italia           | <p>EUR-00023</p><p>IT-00036</p> |
    | Sähköinen PEPPOL-lasku            | Eurooppa          | EUR-00023 |

4. Valitse **Tallenna**.

## <a name="issue-electronic-invoices"></a>Sähköisten laskujen lähettäminen

1. Siirry kohtaan **Organisaation hallinta** \> **Säännölliset** \> **Sähköiset asiakirjat** \> **Lähetä sähköisiä asiakirjoja**.
2. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodatus**.
3. Lisää kyselysuodattimeen taulun nimi valitsemalla **Lisää**.
4. Valitse taulu, joka sisältää laskut.

    > [!NOTE]
    > Taulun nimen on oltava aiemmin tässä ohjeaiheessa [Määritä sovellusasetukset](#configure-the-application-setup) -osassa olevassa taulussa.

5. Valitse taulusta kentän nimi, johon haluat kohdistaa kyselyn.
6. Kirjoita kyselyn ehdoille taulun nimi ja kentän nimi.
7. Lisää kyselyyn kenttiä ja ehtoja toistamalla vaiheita 5 ja 6 ja valitse sitten **OK**.
8. Valitse **OK**.

## <a name="view-submission-logs"></a>Lähetyslokien tarkasteleminen

1. Siirry kohtaan **Organisaation hallinta** \> **Säännölliset** \> **Sähköiset asiakirjat** \> **Sähköisen asiakirjan lähetysloki**.
2. Valitse **Asiakirjatyyppi**-kentässä taulukko, joka sisältää laskut.

    > [!NOTE]
    > Taulun nimen on oltava aiemmin tässä ohjeaiheessa [Määritä sovellusasetukset](#configure-the-application-setup) -osassa olevassa taulussa.

3. Valitse lasku ruudukosta ja valitse sitten **Kysely** \> **Lähetystiedot**.

Maan tai alueen mukaan sähköinen laskutustoiminto saattaa edellyttää lisäkonfiguraatiota. Yksityiskohtaiset vaiheet ovat maasi tai alueesi käytettävissä olenassa aloitusdokumentaatiossa.

## <a name="related-topics"></a>Liittyvät aiheet

- [Sähköisen laskutuksen lisäosan yleiskatsaus](e-invoicing-service-overview.md)
- [Brasilian sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-bra-get-started.md)
- [Meksikon sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-mex-get-started.md)
- [Italian sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-ita-get-started.md)
- [Asiakkaiden sähköiset laskut Egyptissä](emea-egy-e-invoices.md)
