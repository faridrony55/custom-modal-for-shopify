# custom modal for shopify



<style>
  
 

.modal {
    position: fixed;
    z-index: 10000; /* 1 */
    top: 0;
    left: 0;
    visibility: hidden;
    width: 100%;
    height: 100%;
    
    display: flex;
    align-items: center;
    justify-content: center;
}
*{
    scroll-behavior: smooth!important;
}
.modal.is-visible {
    visibility: visible;
}

.modal-overlay {
  position: fixed;
  z-index: 10;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: hsla(0, 0%, 0%, 0.5);
  visibility: hidden;
  opacity: 0;
  transition: visibility 0s linear 0.3s, opacity 0.3s;
}

.modal.is-visible .modal-overlay {
  opacity: 1;
  visibility: visible;
  transition-delay: 0s;
}

.modal-wrapper {
    /*position: fi;*/
    z-index: 9999;
    top: 0;
    left: 50%;
    width: 45em;
    background-color: #fff;
    box-shadow: 0 0 1.5em hsl(0deg 0% 0% / 35%);
    /*margin-top: -125%;*/
    /*margin-left: -11em;*/
}

.modal-transition {
  transition: all 0.3s 0.12s;
  transform: translateY(-10%);
  opacity: 0;
}

.modal.is-visible .modal-transition {
  transform: translateY(0);
  opacity: 1;
}
 
  
 
  @media(max-width:767px){
   
    
.modal-wrapper {
    position: fixed !important;
    z-index: 9999!important;
    top: 50%!important;
    transform: translateY(-50%) !important;
    left: 0%!important;
    width: 100%!important;
    margin-left: 0!important;
    background-color: #fff0!important;
    margin-top: 0!important;
    padding: 10px;
    box-shadow: 0 0 1.5em hsl(0deg 0% 0% / 0%);
}  
.modal-wrapper  iframe{
  height:300px !important;
}
  }
</style>

 <div class="modal">
    <div class="modal-overlay modal-toggle"></div>
    <div class="modal-wrapper modal-transition">
      
      <div class="modal-body">
        <div class="modal-content">
          <iframe width="100%" height="400px" src="https://www.youtube.com/embed/1tUMyVIyiHA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
      </div>
    </div>
  </div>
  


  
  <script>
  $('.modal-toggle').on('click', function(e) {
  e.preventDefault();
  $('.modal').toggleClass('is-visible');
  console.log("hello");
});
  </script>
