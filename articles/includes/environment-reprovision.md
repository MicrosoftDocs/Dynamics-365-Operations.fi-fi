Kun kopioit tietokantaa ympäristöstä toiseen, sinun on varmistettava kaikkien Retail-komponenttien ajantasaisuus suorittamalla ympäristön uudelleenvalmistelutyökalu, jotta kopioitu tietokanta toimisi oikein.

> [!IMPORTANT]
> Suosittelemme, että suoritat tämän toimenpiteen riippumatta siitä, käytetäänkö Retail-komponentteja vai ei, koska Retail-toiminnallisuus sisältyy kaikkiin ympäristöihin. 

Ennen jatkamista sinun on varmistettava, että seuraavat edellytykset täyttyvät:
1. Jos päivität heinäkuun 2017 versioon (tunnetaan myös nimellä 7.2) 7.2.11792.56024, ota käyttöön seuraavat sovelluksen X++ -hotfix-korjaukset kohdeympäristössä ennen tietojen päivityksen suorittamista kyseisessä ympäristössä. Tämä estää tietojen päivityksen aikana tapahtuvia erilaisia virheitä:

    - KB 4036156 – Retail-aliversiopäivitys – Muuttujan numerojärjestystä ei ole määritetty. Tämä paketti sisältää myös korjaukset KB 4035399 ja KB 4035751. Huomaa, että tämän paketin käyttäminen edellyttää vähintään Platform Update 9 -versiota. Jos et ole varma edellytysten täyttymisestä, asenna uusimmat binaaritiedostot.
    
2. Jos päivität Microsoft DynamicsAX 2012 -versiosta, asenna seuraavat sovelluksen X++ -korjaukset kohdeympäristöön ennen tietojen päivityksen suorittamista:
    - KB 4033183 – Dynamics AX 2012 R2- tai Dynamics AX 2012 R3 Pre-CU8 -päivitys (ei-vähittäismyynti) epäonnistuu ja näyttää virheen Objektia ei löydy kohteelle dbo.RETAILTILLLAYOUTZONE.
    - KB 4040692 – Päivitys Dynamics AX 2012 R3 -versiosta Microsoft Dynamics 365 for Operations 7.2 -versioon epäonnistuu: RetailSalesLine-objektin päällekkäinen indeksi kohteessa SalesLineIdx.
    - KB 4035490 – Suorituskykyongelma GeneralJournalAccountEntry-objektin MainAccount-kentän päivityskomentosarjassa.


Suorita ympäristön uudelleenvalmistelutyökalu seuraavien ohjeiden mukaisesti.

1. Valitse jaetussa omaisuuskirjastossa **Käyttöönotettava ohjelmistopaketti**.
2. Lataa ympäristön uudelleenvalmistelutyökalu.
3. Valitse projektin omaisuuskirjastossa **Käyttöönotettava ohjelmistopaketti**.
4. Luo uusi paketti valitsemalla **Uusi**.
5. Kirjoita paketin nimi ja kuvaus. Voit antaa paketin nimeksi **Ympäristön uudelleenvalmistelutyökalu**.
6. Lataa aiemmin lataamasi paketti palvelimeen.
7. Valitse kohdeympäristön **Ympäristön tiedot** -sivulla **Ylläpidä** > **Ota päivitykset käyttöön**.
8. Valitse aiemmin lataamasi ympäristön uudelleenvalmistelutyökalu ja ota sitten paketti käyttöön valitsemalla **Käytä**.
9. Seuraa paketin käyttöönoton edistymistä. 

Lisätietoja käyttöönottopaketin käyttöönotosta on kohdassa [Käyttöönotettavan paketin käyttäminen](../deployment/create-apply-deployable-package.md). Lisätietoja käyttöönottopaketin manuaalisesta käyttöönotosta on kohdassa [Käyttöönotettavan paketin asentaminen](../deployment/install-deployable-package.md).
