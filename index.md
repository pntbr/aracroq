---
layout: page
title: Les acteurs et actrices du circuit-court de la vallée de l'Arac 
---

{% include banner.html %}

Le site Aracroq est un annuaire des personnes qui produisent, élèvent, transforment et distribuent les produits de la vallée de l’Arac. Il met en valeur les circuits courts et le savoir-faire de la vallée, facilite l’accès à des produits de qualité et soutient l’économie locale 

<div id="evenement-banner">
  <p>Evènements à venir !!!</p>
  <ul>
    {% for event in site.evenement %}
      <li>
        <a href="{{ event.url }}">
          {{ event.title | default: event.name }}
        </a>
      </li>
    {% endfor %}
  </ul>
</div>
<style>
#evenement-banner {
  top: 0;
  background: #73d56b;
  border-bottom: 1px solid #002920;
  z-index: 1000;
  padding: 0.5em;
}
#evenement-banner ul {
  list-style: none;
  margin: 0;
  padding: 0;
  gap: 1em;
  flex-wrap: wrap;
  display: flex;
  flex-direction: column;
}
#evenement-banner a {
  text-decoration: none;
  color: #002920;
}
#evenement-banner a:hover {
  text-decoration: underline;
}
</style>

## Annuaire des personnes productrices

<input type="text" id="search-input" placeholder="Rechercher…"   style="padding: 0.5em; font-size: 1em; width: 100%; max-width: 400px; border: 1px solid #ccc; border-radius: 4px; box-sizing: border-box;"
 />
<ul id="results-container"></ul>

<div id="location-nav">
  {% include location-nav.html %}
</div>

<script src="https://unpkg.com/simple-jekyll-search@1.10.0/dest/simple-jekyll-search.min.js"></script>
<script>
  const searchInput = document.getElementById('search-input');
  const locationNav = document.getElementById('location-nav');

  searchInput.addEventListener('input', function () {
    if (this.value.trim() === '') {
      locationNav.style.display = 'block';
    } else {
      locationNav.style.display = 'none';
    }
  });

  SimpleJekyllSearch({
    searchInput: searchInput,
    resultsContainer: document.getElementById('results-container'),
    json: '{{ site.baseurl }}/search.json',
    searchResultTemplate: '<li><a href="{url}">{title}</a></li>',
    noResultsText: 'Aucun résultat',
    limit: 500,
    fuzzy: false,
  });
</script>

- Télécharger l'annuaire en [pdf]({{ site.baseurl }}/assets/pdf/annuaire-personnes-productrices-val-d-Arac.pdf)
- Voir l'annuaire actualisé en [ligne]({{ site.baseurl }}/annuaire.html)

## Présentation

- [Pour qui ?](/pour-qui)
- [Pour quoi ?](/pour-quoi)

## Qui sommes-nous ?

- [Nos valeurs](/nos-valeurs)
- [Nous contacter](/nous-contacter)

## Divers

- [Nous rejoindre](/nous-rejoindre)
- [Liens vers d'autres initiatives](/liens-autres-initiatives)

---

- [Mentions légales et crédits](/mentions)
