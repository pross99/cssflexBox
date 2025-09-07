<script setup>
</script>

<template>


<section>
<div class="grid">
            <div class="card">
                <h1>Responsive grid</h1>
                <div class="content">
                    <p>
                        The columns show a grid pattern that has cards with a minimum of 300px width. The maximum width is "1fr", meaning they can grow to take up available space in the container
                    </p>
                </div>
            </div>

            <div class="card">
                <div class="video-responsive">
                    <div>
                        <iframe 
                        src="https://www.youtube.com/embed/xvFZjo5PgG0" 
                        title="YouTube video player" 
                        frameborder="0" 
                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                        referrerpolicy="strict-origin-when-cross-origin" 
                        allowfullscreen>
                        </iframe>
                     
                    </div>
                </div>
                <h1>Adaptive Video Container</h1>
                <div class="content">
                    <p>Video content automatically maintains its aspect ratio across all screen sizes. The container uses percentage-based padding to create a responsive 16:9 ratio that works on any device.</p>
                </div>
            </div>

            <div class="card">
                <h1>Responsive text</h1>
                <div class="content">
                    <p>The text in this app uses the CSS <code>clamp()</code> to have a trylu responsive font-size.. </p>
                    <code>  p{
    font-size: clamp(1rem, 2.5vw, 2rem);
  }</code>

                </div>
                
            </div>

            <div class="card">
                <h1>CSS Grid Auto-Fit</h1>
                <div>
                  <p>  The main grid uses <code>auto-fit</code> with <code>minmax()</code> to automatically adjust the number of columns based on available space. Items have a minimum width of 300px and grow to fill available space equally.</p>
                </div>
            </div>

            <div class="card">
                <h1>Media Queries</h1>
                <p>until now, no media queries have been used to help with CSS on different viewports. media quieries can however still be used for other usecasesr</p>
            </div>

            <div class="card">
                <h1>Advanced Media Queries</h1>
                <p>
                    • <strong>Color Scheme:</strong> Automatic dark mode support
                    <br>
                    • <strong>Motion:</strong> Respects reduced motion preferences
                    <br>
                    • <strong>Print:</strong> Optimized print stylesheet
                </p>
            </div>
        </div>
            
</section>
</template>

<style lang="scss" scoped>

section{
   max-width: 100svw;
   height: 100svh;
   margin: 0 auto;
   padding: 20px;

}

.grid{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap:2rem;
    margin-bottom: 3rem;
}

.card{
    padding: 2rem;
    border-radius: 1rem;
    background-color: beige;
}

.video-responsive{
       position: relative;
            padding-bottom: 56.25%; /* 16:9 aspect ratio */
            height: 0;
            overflow: hidden;
            border-radius: 10px;

            iframe{
                  position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
            border-radius: 10px; 
            }
}




 @media (prefers-color-scheme: dark) {
            .grid {
                background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
            }
            
            .card {
                background: rgba(255, 255, 255, 0.1);
                color: white;
                backdrop-filter: blur(15px);
            }
            
            .card h3 {
                color: #74b9ff;
            }
        }


  @media (prefers-reduced-motion: reduce) {
            * {
                animation-duration: 0.01ms !important;
                animation-iteration-count: 1 !important;
                transition-duration: 0.01ms !important;
            }
        }

        @media print {
            body {
                background: white;
                color: black;
            }
            
            .card {
                background: green;
                box-shadow: none;
                border: 1px solid #ccc;
            }
            
            .breakpoint-indicator {
                display: none;
            }
        }
</style>