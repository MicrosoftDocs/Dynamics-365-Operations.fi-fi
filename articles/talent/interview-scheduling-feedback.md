---
title: Haastattelujen aikataulutus ja palaute
description: Tässä ohjeaiheessa on tietoja haastattelujen aikataulutus- ja palautetehtävistä Attractissa.
author: ''
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: hasrivas
ms.openlocfilehash: 7bc5a66bb221cb0ab2c69fcb1013ed48a7c664a6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2019
ms.locfileid: "374891"
---
# <a name="interview-scheduling-and-feedback"></a>Haastattelujen aikataulutus ja palaute

[!include[banner](../includes/banner.md)]

## <a name="scheduler-activity"></a>Ajastus-tehtävä

Valinnaisessa ajastustehtävässä on kaksi osaa: ehdokkaan käytettävyystietojen pyytäminen ja aikataulu. Ehdokkaan käytettävyystiedot -osassa voit pyytää ehdokkaan käytettävyystietoja sähköpostitse. Aikataulu-osassa voi sopia haastattelun ajankohdan ehdokkaan ja työhönottoryhmän kesken.

### <a name="candidate-availability-request"></a>Ehdokkaan käytettävyystietojen pyytäminen

Jos haluat pyytää ehdokkaiden käytettävyystietoja sähköpostitse, valitse **Pyydä ehdokkaan käytettävyystietoja** -kenttä. Jos kenttää ei valita, tätä vaihetta ei näytetä työn työhönottoprosessissa.

Voit pyytää käytettävyystietoja valitsemalla ensin **Lähetä pyyntö** ja sitten käytettävissä olevat päivämäärät ja sähköpostimallin. Lähetä sähköposti tämän jälkeen ehdokkaalle.

[![Attractin työhönottajan näkymä ehdokkaan käytettävyystietojen pyytämiseen](./media/scheduler-candidate-request.png)](./media/scheduler-candidate-request.png)

Kun ehdokas saa sähköpostiviestin, jossa häntä pyydetään vastaamaan pyyntöön, hän voi kirjautua ehdokasportaaliin, valita ensin hänelle sopivat päivämäärät ja valitse sitten **Lähetä**.

### <a name="schedule"></a>Aikataulu
Haastattelun ajastuksessa on useita määrityksiä, joiden avulla haastattelijoille ja ehdokkaalle lähetettävä haastatteluryhmä voidaan luoda.

1. Valitse **Luo aikataulu** ja lisää sitten **Lisää haastattelijoita** -ruudussa luetteloon kaikki haastattelijat, jotka tulevat haastatteluryhmään.
[![Attractin työhönottajanäkymän haastatteluryhmän ajoittamisen aloittamisesta](./media/schedule-start-over.png)](./media/schedule-start-over.png)   
    Jos ehdokas on vastannut haastattelun käytettävyystietopyyntöön, heidän valintansa on valmiina **Haastattelupvm**-kentässä. Voit valita tarvittaessa toisen päivämäärän.
    
    Jos valitset **Tee tästä paneelihaastattelu** -kentän, haastattelu luodaan siirtämällä vasemmalla oleva haastattelijaryhmä yhteen paneeliryhmään. Seuraavaksi on määritettävä haastattelujärjestys.
    
    Haastatteluaikataulu on järjestettävä siten, että se vastaa parhaiten osallistujien käytettävyystietoja. Jos kyse on sisäisestä hakijasta, voit sisällyttää heidän käytettävyystietonsa osaksi aikataulusuositusta.
    
    Jos haluat järjestää verkkotapaamisen, valitse **Lisää Skype-tapaamisia** -kenttä, jonka jälkeen jokaisessa haastattelutapahtumassa on **Skype for Business** -linkki.

2. Valitse kunkin haastattelutapahtuman kesto ja aloita sitten aikataulun luonti valitsemalla **OK**.

    Jos **Suositukset** on valittu, näkyviin tulee ehdotuksia ja haastatteluruudukko on täytetty valmiiksi. Näkyviin tulee kalanteri, jossa näkyy kaikkien valittujen haastattelijoiden käytettävyystiedot. Voit tarkastella myös sisäisen ehdokkaan kalenteria.

3. Jos ehdotuksia ei ole, napsauta **Haastattelijat**-sarakkeessa ajankohtaa, lisää haastattelun otsikko ja tiedot sekä täytä tarvittaessa sijaintitiedot. Voit halutessasi sisällyttää haastattelun **Skype for Business** -linkin.

4. Voit lisätä muita haastattelijoita valitsemalla haastattelijoita napsauttamalla **Lisää haastattelu** -ruudukon saraketta. Voit poistaa haastattelun ryhmästä kolme pistettä (...) -asetuksella.
    
5. Jos haastattelut on aikataulutettu ei aikavyöhykkeelle, valitse sopiva kaupunki/aikavyöhyke avattavasta luettelosta oikeassa yläkulmassa. Haastattelijan käytettävyysruudukko päivitetään vastaamaan uutta aikavyöhykettä. Tämä aikavyöhykevalinta näkyy nyt myös **Haastattelun yhteenveto** -näkymässä, joka jaetaan haastattelijoiden ja ehdokkaan kanssa. 

6. Lähetä kokouskutsut asianomaisille haastattelijoille valitsemalla **Lähetä haastattelijoille**.

    Sen jälkeen kun haastattelupyynnöt on lähetetty haastattelijoille, he voivat vastata suoraan heille lähetetystä sähköpostikutsusta.

    >[!NOTE]
    > Kaikkien yksilöhaastattelujen muistutukset lähetetään haastattelijoille 24 tunnin välein, jos haastattelija ei vastaa (hyväksyy tai hylkää) haastattelupyyntöön.

    > Paneelihaastatteluilla ei ole automaattisia muistutuksia haastattelupyynnöstä. Voit käynnistää muistutuksen manuaalisesti muokkaamalla haastattelua ja lähettämällä pyynnön takaisin haastattelijoille **Päivitä ja lähetä** -asetuksella.

    Haastattelijan vastaukset taltioidaan ja näytetään Attractissa. Jos haastattelija hylkää kutsun, sinua pyydetään tekemään muutos. Voit tarkastella vastausta **Ajoitus**-ruudukkonäkymässä puhekuplakuvaketta napsauttamalla.

[![Attractin työhönottaja näkymä haastattelijan vastauksesta](./media/schedule-interviewer-response.png)](./media/schedule-interviewer-response.png)

7. Kun haastatteluaikataulu on valmis ehdokkaan kanssa jaettavaksi, valitse **Lähetä ehdokkaalle**. Voit valita, piilotetaanko vai näytetäänkö haastattelijoiden nimet ja ajat ehdokkaalle.

8. Valitse sähköpostimalli ja lähetä haastattelun yhteenveto ehdokkaalle. Ehdokas voi tarkastella näitä tietoja sekä sähköpostissa että ehdokasportaalissa.
    
>[!NOTE] 
> Käytettävyystiedot näytetään ehdokkaan kalenterissa vain, jos kyse on sisäisestä ehdokkaasta. Samalla tavoin vain sisäisen ehdokkaan tietoja voidaan käyttää haastattelun aikataulusuosituksissa. Tällä hetkellä ehdokkaat (sisäiset tai ulkoiset) eivät saa kokouskutsua sähköpostitse, vaan ehdokas saa vain haastattelujen yhteenvedon.

## <a name="feedback-activity"></a>Palaute-tehtävä

Palautetehtävä on työmallissa valinnainen. Tämän tehtävän avulla haastatteluun osallistuvat voivat antaa hakijaa koskevia suosituksia tai palautekommentteja. Jos **Peri palautteeseen osallistujat työhönottoryhmältä** -kenttä valitaan, työnottaja, työhön ottava esimies ja haastattelijat siirtyvät automaattisesti palautetehtävään. Organisaatiot voit antaa haastattelijoille mahdollisuuden tarkastella muiden palautteet, ennen kuin he lähettävät oman palautteensa. Organisaatiot voivat lisäksi antaa haastattelijoille mahdollisuuden muokata jo lähetettyä palautetta. Haastattelijoita muistutetaan heidän äskettäin suorittamiensa haastattelujen palautteen lähettämisestä. Tämä muistutus perustuu työmallin osana tehtyihin valmiisiin määrityksiin. Työn työhön ottava esimies tai työhönottaja voivat halutessaan muistuttaa haastattelijaa palautteen lähettämisestä myös manuaalisesti.

## <a name="interview-activity"></a>Haastattelu-tehtävä

Valinnaisessa haastattelutehtävässä on kolme osaa: ehdokkaan käytettävyystietojen pyytäminen, aikataulu ja palaute. Käytä haastattelutehtävää työmallissa, jos haluat, että ehdokkaan käytettävyystietojen pyyntö, aikataulu ja palaute ovat kaikki prosessin osia sen sijaan, että niitä käytettäisiin erikseen työhönottoprosessin osina.
