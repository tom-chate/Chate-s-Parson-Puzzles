---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Home Page
---
<div class="carousel-inner">

  <!-- Slide 1: Parson puzzle -->
  <div class="carousel-item active">
    <div class="d-flex flex-column flex-md-row align-items-center justify-content-between p-4 bg-light rounded">
      <div>
        <h2 class="h4 mb-2">Try a Parson Puzzle</h2>
        <p class="mb-0">
          Practice GCSE programming skills with interactive Parsons puzzles.
        </p>
      </div>
      <a
        class="btn btn-primary mt-3 mt-md-0"
        href="{{ '/parsons/passwords-condition-controlled.html' | relative_url }}">
        Start with: Passwords Puzzle
      </a>
    </div>
  </div>

  <!-- Slide 2: GCSE grade calculator -->
  <div class="carousel-item">
    <div class="d-flex flex-column flex-md-row align-items-center justify-content-between p-4 bg-light rounded">
      <div>
        <h2 class="h4 mb-2">GCSE Total Grade Calculator</h2>
        <p class="mb-0">
          Work out your total GCSE points using a count-controlled loop.
        </p>
      </div>
      <a
        class="btn btn-success mt-3 mt-md-0"
        href="{{ '/parsons/GCSE-total-grade-calc.html' | relative_url }}">
        Open calculator
      </a>
    </div>
  </div>

  <!-- Slide 3: YouTube -->
  <div class="carousel-item">
    <div class="d-flex flex-column flex-md-row align-items-center justify-content-between p-4 bg-light rounded">
      <div>
        <h2 class="h4 mb-2">Watch on YouTube</h2>
        <p class="mb-0">
          See walkthroughs and explanations for Ed-Chate activities.
        </p>
      </div>
      <a
        class="btn btn-danger mt-3 mt-md-0"
        href="https://www.youtube.com/@edu-chate"
        target="_blank"
        rel="noopener">
        Visit channel
      </a>
    </div>
  </div>
  <button class="carousel-control-prev" type="button"
        data-bs-target="#homeCarousel" data-bs-slide="prev">
  <span class="carousel-control-prev-icon" aria-hidden="true"></span>
  <span class="visually-hidden">Previous</span>
</button>

<button class="carousel-control-next" type="button"
        data-bs-target="#homeCarousel" data-bs-slide="next">
  <span class="carousel-control-next-icon" aria-hidden="true"></span>
  <span class="visually-hidden">Next</span>
</button>


</div>
