

<a > <img width ='100%'  height ='5px' src ='https://upload.wikimedia.org/wikipedia/commons/b/bf/GradientPurpleBlue.png'> </a>
### One Click Website! 


<div id="smart-button-container">
      <div style="text-align: center;">
        <div style="margin-bottom: 1.25rem;">
          <p>One Click Website!</p>
          <select id="item-options"><option value="Linktree" price="74">Linktree - 74 EUR</option><option value="Portfolio" price="250">Portfolio - 250 EUR</option><option value="Small or Local Bussiness" price="750">Small or Local Bussiness - 750 EUR</option><option value="Blog" price="950">Blog - 950 EUR</option><option value="Shop/Store" price="1750">Shop/Store - 1750 EUR</option></select>
          <select style="visibility: hidden" id="quantitySelect"></select>
        </div>
      <div id="paypal-button-container"></div>
      </div>
    </div>
    <script src="https://www.paypal.com/sdk/js?client-id=sb&enable-funding=venmo&currency=EUR" data-sdk-integration-source="button-factory"></script>
    <script>
      function initPayPalButton() {
        var shipping = 0;
        var itemOptions = document.querySelector("#smart-button-container #item-options");
    var quantity = parseInt();
    var quantitySelect = document.querySelector("#smart-button-container #quantitySelect");
    if (!isNaN(quantity)) {
      quantitySelect.style.visibility = "visible";
    }
    var orderDescription = 'One Click Website!';
    if(orderDescription === '') {
      orderDescription = 'Item';
    }
    paypal.Buttons({
      style: {
        shape: 'rect',
        color: 'black',
        layout: 'vertical',
        label: 'paypal',
        
      },
      createOrder: function(data, actions) {
        var selectedItemDescription = itemOptions.options[itemOptions.selectedIndex].value;
        var selectedItemPrice = parseFloat(itemOptions.options[itemOptions.selectedIndex].getAttribute("price"));
        var tax = (0 === 0 || false) ? 0 : (selectedItemPrice * (parseFloat(0)/100));
        if(quantitySelect.options.length > 0) {
          quantity = parseInt(quantitySelect.options[quantitySelect.selectedIndex].value);
        } else {
          quantity = 1;
        }

        tax *= quantity;
        tax = Math.round(tax * 100) / 100;
        var priceTotal = quantity * selectedItemPrice + parseFloat(shipping) + tax;
        priceTotal = Math.round(priceTotal * 100) / 100;
        var itemTotalValue = Math.round((selectedItemPrice * quantity) * 100) / 100;

        return actions.order.create({
          purchase_units: [{
            description: orderDescription,
            amount: {
              currency_code: 'EUR',
              value: priceTotal,
              breakdown: {
                item_total: {
                  currency_code: 'EUR',
                  value: itemTotalValue,
                },
                shipping: {
                  currency_code: 'EUR',
                  value: shipping,
                },
                tax_total: {
                  currency_code: 'EUR',
                  value: tax,
                }
              }
            },
            items: [{
              name: selectedItemDescription,
              unit_amount: {
                currency_code: 'EUR',
                value: selectedItemPrice,
              },
              quantity: quantity
            }]
          }]
        });
      },
      onApprove: function(data, actions) {
        return actions.order.capture().then(function(orderData) {
          
          // Full available details
          console.log('Capture result', orderData, JSON.stringify(orderData, null, 2));

          // Show a success message within this page, e.g.
          const element = document.getElementById('paypal-button-container');
          element.innerHTML = '';
          element.innerHTML = '<h3>Thank you for your payment!</h3>';

          // Or go to another URL:  actions.redirect('thank_you.html');

        });
      },
      onError: function(err) {
        console.log(err);
      },
    }).render('#paypal-button-container');
  }
  initPayPalButton();
    </script>





<center>


| Linktree | Blog | Store |
| --- |  --- | --- |
| [![Chalk](https://raw.githubusercontent.com/nielsenramon/chalk/master/_assets/images/documentation/chalk-intro%402x.png)<a href="" class="blockoPayBtn" data-toggle="modal" data-uid=3a3a3b2c8e6711eb><img width=160 src="https://www.blockonomics.co/img/pay_with_bitcoin_medium.png"></a>](https://github.com/nielsenramon/chalk) | [![TeXt](https://raw.githubusercontent.com/kitian616/jekyll-TeXt-theme/master/screenshots/TeXt-home.jpg)<a href="" class="blockoPayBtn" data-toggle="modal" data-uid=3a3a3b2c8e6711eb><img width=160 src="https://www.blockonomics.co/img/pay_with_bitcoin_medium.png"></a>](https://github.com/kitian616/jekyll-TeXt-theme) | [![Anatole](https://raw.githubusercontent.com/lxndrblz/anatole/master/images/screenshot.png)<a href="" class="blockoPayBtn" data-toggle="modal" data-uid=3a3a3b2c8e6711eb><img width=160 src="https://www.blockonomics.co/img/pay_with_bitcoin_medium.png"></a>](https://github.com/lxndrblz/anatole) |
| Portfolio | TeXt | Anatole |
| [![Chalk](https://raw.githubusercontent.com/nielsenramon/chalk/master/_assets/images/documentation/chalk-intro%402x.png)](https://github.com/nielsenramon/chalk) | [![TeXt](https://raw.githubusercontent.com/kitian616/jekyll-TeXt-theme/master/screenshots/TeXt-home.jpg)](https://github.com/kitian616/jekyll-TeXt-theme) | [![Anatole](https://raw.githubusercontent.com/lxndrblz/anatole/master/images/screenshot.png)](https://github.com/lxndrblz/anatole) |
| Chalk | TeXt | Anatole |
| [![Chalk](https://raw.githubusercontent.com/nielsenramon/chalk/master/_assets/images/documentation/chalk-intro%402x.png)](https://github.com/nielsenramon/chalk) | [![TeXt](https://raw.githubusercontent.com/kitian616/jekyll-TeXt-theme/master/screenshots/TeXt-home.jpg)](https://github.com/kitian616/jekyll-TeXt-theme) | [![Anatole](https://raw.githubusercontent.com/lxndrblz/anatole/master/images/screenshot.png)](https://github.com/lxndrblz/anatole) |


</center>


## Useful Tools and links:


Emoji | [Emojipedia.org](https://emojipedia.org/) | [on Github](https://gist.github.com/rxaviers/7360908)| [on Dev.to](https://dev.to/nikolab/complete-list-of-github-markdown-emoji-markup-5aia) | :smile: :grin: :cry: 

Icons | [Simpleicons.org](https://simpleicons.org/?q=netl) |  <a> <img width ='20px' src ='https://raw.githubusercontent.com/rahulbanerjee26/githubAboutMeGenerator/main/icons/reactjs.svg'> </a>
<a> <img width ='20px' src ='https://raw.githubusercontent.com/rahulbanerjee26/githubAboutMeGenerator/main/icons/javascript.svg'> </a>
 <a> <img width ='20px' src ='https://raw.githubusercontent.com/rahulbanerjee26/githubAboutMeGenerator/main/icons/python.svg'> </a> 

Gif Libraries | [on Github](https://gifs.joelglovier.com/) | <a> <img src = "https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/wave.gif" width = 20px> 

Badge | [Shield.io](https://shields.io/category/social) | [Aleen42](https://github.com/aleen42/badges) | [![Badges](https://img.shields.io/badge/Cool-Badges-1462ab.svg?)](https://shields.io) 

Pictures/Photos | [Pexels](https://www.pexels.com/) | [Wikipedia](https://commons.wikimedia.org/wiki/Category:Images) | [Slickr](https://slickr.vercel.app/app) |:camera:

Markdown Editors | [jbt](https://jbt.github.io/markdown-editor/) | [Cool](https://coolmarkdowneditor.org/) | [Upmath](https://upmath.me/) | <a> <img width ='20px' src ='https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/markdown/markdown.png'> </a> 

List of Static Site generators | [Jamstack.org](https://jamstack.org/generators/)

Automation | [Integromat](https://www.integromat.com) | [zapier](https://zapier.com/) | [ifttt](https://ifttt.com/) | ⚙️ 

Cross blog | [Dev.to](https://www.dev.to) | [Medium](https://medium.com/) | [Hashnode](https://hashnode.com/@PRIM4T/joinme) | :pencil:


<a> <img width ='100%'  height ='5px' src ='https://upload.wikimedia.org/wikipedia/commons/b/bf/GradientPurpleBlue.png'> </a>


Made with with ❤️ and 💪 by [PRIM4T](https://www.prim4t.art) \
Feel free [contribute!](https://github.com/prim4t/Web-Setup-Essentials)


[![Tip Me via PayPal](https://img.shields.io/badge/PayPal-tip%20me-1462ab.svg?logo=paypal)](https://www.paypal.me/prim4tdotart)
[![Tip Me via Bitcoin](https://img.shields.io/badge/Bitcoin-tip%20me-f7931a.svg?logo=bitcoin)](https://raw.githubusercontent.com/kitian616/jekyll-TeXt-theme/master/docs/assets/images/3Fkufxcw2xd8HnaRJBNK4ccdtkUDyyNu4V.jpg)


<a href="" class="blockoPayBtn" data-toggle="modal" data-uid=3a3a3b2c8e6711eb><img width=160 src="https://www.blockonomics.co/img/pay_with_bitcoin_medium.png"></a>

<script src="https://www.blockonomics.co/js/pay_button.js"></script>
