You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "Gabapentin.html",
    "context": {
      "title": "Welcome To LELEON LIFE SCIENCE",
      "first_heading": "Gabapentin-Nortriptyline"
    }
  },
  {
    "path": "LELEON-AS-Backup.html",
    "context": {
      "title": "Available services | Leleon",
      "first_heading": "LELEON AS"
    }
  },
  {
    "path": "LELEON-AS.html",
    "context": {
      "title": "Available services | Leleon",
      "first_heading": "LELEON AS"
    }
  },
  {
    "path": "LELEON-D-GEL.html",
    "context": {
      "title": "Available services | Leleon",
      "first_heading": "LELEON D GEL"
    }
  },
  {
    "path": "LELEON-PLUS.html",
    "context": {
      "title": "Available services | Leleon",
      "first_heading": "LELEON PLUS"
    }
  },
  {
    "path": "LELEONCLAV-625-MG.html",
    "context": {
      "title": "Available services | Leleon",
      "first_heading": "LELEONCLAV 625 MG"
    }
  },
  {
    "path": "Paroxetine.html",
    "context": {
      "title": "Welcome To LELEON LIFE SCIENCE",
      "first_heading": "DeUPa 12.5mg and 25mg tablets"
    }
  },
  {
    "path": "YTIDICA.html",
    "context": {
      "title": "Available services | Leleon",
      "first_heading": "YTIDICA (PANTAPROZOLE 40MG)"
    }
  },
  {
    "path": "about.html",
    "context": {
      "title": "Leleon Life Science | About",
      "first_heading": "About Us"
    }
  },
  {
    "path": "contact.html",
    "context": {
      "title": "Leleon Life Science | Contacts",
      "first_heading": "Contact Us"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/6cf61212db3fabb4a22c2f2855cc3970.css",
    "context": {
      "path": "css/6cf61212db3fabb4a22c2f2855cc3970.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "esrey.html",
    "context": {
      "title": "Welcome To LELEON LIFE SCIENCE",
      "first_heading": "ESREY 5MG AND 10 MG (Escitalopram)"
    }
  },
  {
    "path": "flunaprop.html",
    "context": {
      "title": "FLUNAPROP | FLUNARIZINE 10mg and PROPRANOLOL SR 40MG",
      "first_heading": "FLUNAPROP(FLUNARIZINE 10mg and PROPRANOLOL SR 40MG)"
    }
  },
  {
    "path": "imgs/0639e149a84172038b4679090ea84054.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/16f6ba8fdbfb447488d2ce4a372450f1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2781d9a53a9ff6e832919a41ff27e27f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2b3c2b6b95ab7c6e67833d8c1eee4718.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2c87657a7d8254ebc32acfbb7c8aec79.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2e89841ba17c336ea351ea461c1fb6bb.webp",
    "context": {
      "refs": [
        {
          "alt": "LELEON AS",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/30173cf639ef12082beb144920fe859a.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/430f68e703f32f0cb401877778848108.webp",
    "context": {
      "refs": [
        {
          "alt": "HEALTH CARE",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4e56edcc0b4e095c99aaf5075ea37bba.webp",
    "context": {
      "refs": [
        {
          "alt": "YTIDICA (PANTAPROZOLE 40MG)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/608e380b65fea87af8b7f5afea22d0bc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/73a547cd4076941f27c4f6ceae0885ee.webp",
    "context": {
      "refs": [
        {
          "alt": "LELEONCLAV 625 MG",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/88dbe45ad42e29981c8e0c408b29f7ef.webp",
    "context": {
      "refs": [
        {
          "alt": "LELEON PLUS",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8dfbe45df583a5c3805e78eaa9680a28.webp",
    "context": {
      "refs": [
        {
          "alt": "PRODUCTS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/99dcd9d8f33bb6390ca53eafea8c465c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9efa400127b11cdbb26098bafd007c5d.webp",
    "context": {
      "refs": [
        {
          "alt": "Medical uses",
          "title": ""
        },
        {
          "alt": "Medical uses",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0d8a52af9705875479716cc31092feb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c849c1a989ba9910df78ebef2d597274.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d010ce0c485115355ba4b114f71b4f28.webp",
    "context": {
      "refs": [
        {
          "alt": "About us",
          "title": ""
        },
        {
          "alt": "Leleon Life Science",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d23e8f745b9bb6b7e90dee20a2b1d158.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dfc4fe19d922cca067601126556550a7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e258cb1b156134e9c64a6a46ddfeb9d8.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e657ea2f7bde607d3fe5dad14a6960ea.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec3cce0ea2020253d4e0cecfa87d8955.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fc3623d4c956259292bd2e9728a5bdb7.webp",
    "context": {
      "refs": [
        {
          "alt": "Diclofenac Diethylamine 1.16% + Linseed Oil 3% + Methyl Salicylate 10% + Menthol 5%+ benzyl alcohol ",
          "title": ""
        },
        {
          "alt": "LELEON D GEL",
          "title": ""
        },
        {
          "alt": "Diclofenac Diethylamine 1.16% + Linseed Oil 3% + Methyl Salicylate 10% + Menthol 5%+ benzyl alcohol ",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fdbde576216f27c5795d27f75e9b5e7a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Welcome To LELEON LIFE SCIENCE",
      "first_heading": "Welcome To LELEON LIFE SCIENCE"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "le-os-care.html",
    "context": {
      "title": "Welcome To LELEON LIFE SCIENCE",
      "first_heading": "Le-Os-Care"
    }
  },
  {
    "path": "our-distributors.html",
    "context": {
      "title": "Leleon Life Science | Our Distributors",
      "first_heading": "Our Distributors"
    }
  },
  {
    "path": "qutacron.html",
    "context": {
      "title": "Welcome To LELEON LIFE SCIENCE",
      "first_heading": "QUTACRON 50MG AND 100MG SCORED TAB(QUETIAPINE)"
    }
  },
  {
    "path": "services.html",
    "context": {
      "title": "Available services | Leleon",
      "first_heading": "Services"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.