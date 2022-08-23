---
title: Muiden osavaltioiden toimittajien tuotteiden ICMS-DIF-verolaskelmien muutoksen perusta
description: Tässä artikkelin kuvataan ICMS-DIF-verotyypin laskelmien konfiguraatio, kun veroasiakirja vastaanotetaan Brasilian Rio Grande do Sulin (RS) tai São Paulon (SP) osavaltiossa.
author: Kai-Cloud
ms.date: 06/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 1bd9982a3804778a27203b4311682ee8bc3c4841
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218646"
---
# <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Muiden osavaltioiden toimittajien tuotteiden ICMS-DIF-verolaskelmien muutoksen perusta (kaksoiskanta)

Tässä artikkelin kuvataan **ICMS-DIF**-verotyypin laskelmien konfiguraatio, kun veroasiakirja vastaanotetaan Brasilian Rio Grande do Sulin (RS) tai São Paulon (SP) osavaltiossa.

Valtion lain määritelmän mukaan kerätyn Imposto sobre Circulação de Mercadorias e Serviçosin (ICMS) on noudatettava tätä sääntöä:

*ICMS kerää* = ([(*Toiminnan määrä* – *ICMS lähteestä*) ÷ (1 – *ICMS % sisäinen*)] × *ICMS % sisäinen*) – *ICMS-määrä lähteestä*

## <a name="example"></a>Esimerkki

Brasilialainen RS-tilassa oleva yritys saa veroasiakirjan ostosta SP-tilassa olevalta toimittajalta. Yrityksen on kerättävä ICMS: n prosentuaalinen ero RS-valtion (18 prosenttia) ja SP-tilan (12 prosenttia) välillä. Pohja on kuitenkin laskettava edellisen säännön mukaisesti.

- **Operaation summa:** 1 000,00 Brasilian realia (1 000,00 R$)
- **ICMS osavaltioiden välinen:** 120,00 R$
- **ICMS-prosenttiosuus RS-tilassa:** 18 prosenttia
- **RS-tilassa kerättävä ICMS:** (\[(1 000 – 120) ÷ (1 – 0,18)\] × 0,18 ) – 120 = 73,17 R$ 

## <a name="resolution"></a>Ratkaisu

Jos haluat laskea differentiaali-ICMS:n (ICMS-DIF) RS-osavaltion sääntöjen mukaisesti, sinun on määritettävä arvonlisäverokoodit ja arvonlisäveroryhmä seuraavasti:

1. Luo arvonlisäverokoodi, joka vastaanottaa 12 prosentin ICMS:n (toisessa osavaltiossa). Tätä koodia käytetään rekisteröimään toimittajan verosaatavien summa.
2. Luo arvonlisäverokoodi ICMS-DIF:n keräämiseksi. Tämän arvonlisäverokoodin prosenttiosuuden on oltava 18 prosenttia (omassa valtiossasi), joka määrittää 18–12 prosentin eron. Määritä verotyypiksi **ICMS-DIF**. Tämä arvonlisäverokoodi on määritettävä laskentaparametreissa seuraavasti:

    - Valitse **Alkuperä**-kentässä **Bruttosumman prosenttiosuus**.
    - Valitse **Alv-rajan peruste** -kentässä **Rivikohtainen nettosumma**.
    - Määritä verotuskoodi siten, että sen verotuksellinen arvo on **3**. Tällä tavoin oikaisutapahtuma luodaan automaattisesti, kun **Verokirjat**-moduuli on käytössä.
    - Valitse arvonlisäveroryhmän konfiguraatiossa **ICMS-DIF**-arvonlisäverokoodin **Käyttövero**-vaihtoehto.

### <a name="use-the-delta-tax-rate-in-the-configuration-of-dual-base-icms-dif-sales-tax-codes"></a>Deltaverokantaa käytetään ICMS-DIF-arvonlisäverokoodien kaksoiskannan määrityksessä

Kun aiemmin kuvattuja asetuksia käytetään, **ICMS-DIF**-arvonlisäverokoodi lasketaan kaksoiskantasäännöllä. Kuitenkin nimellisveroprosentista tulee 18 prosenttia, joka eroaa yksinkertaisen perussäännön 6 prosentista. Tämä ero aiheuttaa ristiriitaongelmia veroasiakirjassa ja veroilmoituksessa. Microsoft Dynamics 365 Financen versiosta 10.0.29 alkaen voit ottaa käyttöön **(Brasilia) Aseta ICMS-DIF-verokoodin deltaverokanta kaksoiskantatilanteissa** -ominaisuuden **toimintojen hallinnassa**. Näin voit poistaa ristiriidan.

- Edellisen osan vaiheiden suorittamisen lisäksi valitse **ICMS 12**-arvonlisäverokoodi **Arvonlisäveron arvonlisävero** -kentässä.
- Määritä **ICMS-DIF**-arvonlisäverokoodin veroprosentiksi 18 prosenttia. **Prosenttiosuus/summa**-kentässä nimellisveroprosentti on 6 prosenttia.

> [!NOTE]
> **ICMS-DIF**- ja **ICMS 12** -arvonlisäverokoodit on liitettävä samaan arvonlisäveroryhmään.

## <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-to-non-taxpayer-consumers-difal-in-other-states"></a>ICMS-DIF-verolaskelmien muutoksen perusta (kaksoiskanta) tuotteille muille kuin verovelvollisille kuluttajille (DIFAL) muissa osavaltioissa

Ota käyttöön **(Brasilia) Myyntitapahtumien ICMS-DIFAL-kaksoiskannan laskenta** -ominaisuus **toimintojen hallinnassa** ICMS-DIF-verolaskelmien muutoksen perustan tukemiseksi kaupankäynnissä muille kuin verovelvollisille kuluttajille toisesta osavaltiosta. ICMS-DIF-arvonlisäverokoodi-malli tulee voimaan myyntitilaus- ja vapaatekstilaskutapahtumissa.

Ota käyttöön **(Brasilia) IPI-tapausten ICMS-DIFAL-kaksoiskannan laskenta** -ominaisuus **toimintojen hallinnassa**. Sen avulla voidaan tukea skenaarioita, joissa kaupankäynti toisen osavaltion muille kuin verovelvollisille kuluttajille on vastuussa Imposto sobre Produtos Industrializados (IPI) -verosta. IPI-arvonlisäverokoodin veron summa tunnistetaan ja sitä sovelletaan ICMS-DIFAL -veron perusteena.

- Myyntitilauksen tai vapaatekstilaskun otsikon **Verotiedot**-pikavälilehden **Lopullinen käyttäjä** -asetuksena on oltava **Kyllä**.
- Ostotilauksen tai toimittajan laskun otsikon **Verotiedot**-pikavälilehden **Käyttö ja kulutus** -asetuksena on oltava **Kyllä**.
