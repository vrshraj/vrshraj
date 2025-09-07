<!-- Save this as assets/tictactoe.svg -->
<svg xmlns="http://www.w3.org/2000/svg" width="600" height="200" viewBox="0 0 600 200" role="img" aria-label="Tic Tac Toe animation">
  <style>
    .board-line { stroke:#2b2b2b; stroke-width:6; stroke-linecap:round; }
    .x { stroke:#e63946; stroke-width:10; stroke-linecap:round; stroke-linejoin:round; fill:none; }
    .o { stroke:#457b9d; stroke-width:10; fill:none; stroke-linecap:round; }
  </style>

  <!-- 3x3 grid (3 columns shown twice for a horizontal strip layout) -->
  <!-- We'll draw a single 3x3 board and animate plays on it -->
  <g transform="translate(50,10) scale(1)">
    <!-- grid background -->
    <rect x="0" y="0" width="180" height="180" rx="12" fill="#fbfbfb" stroke="#e6e6e6" stroke-width="2"/>

    <!-- vertical lines -->
    <line x1="60" y1="10" x2="60" y2="170" class="board-line" />
    <line x1="120" y1="10" x2="120" y2="170" class="board-line" />
    <!-- horizontal lines -->
    <line x1="10" y1="60" x2="170" y2="60" class="board-line" />
    <line x1="10" y1="120" x2="170" y2="120" class="board-line" />

    <!-- Coordinates for cells:
         top-left (40,40), top-mid (100,40), top-right (160,40)
         mid-left (40,100), mid-mid (100,100), mid-right (160,100)
         bot-left (40,160), bot-mid (100,160), bot-right (160,160)
    -->

    <!-- X at top-left -->
    <g transform="translate(40,40)">
      <line x1="-20" y1="-20" x2="20" y2="20" class="x">
        <animate attributeName="stroke-dasharray" from="0,56" to="56,0" dur="350ms" begin="0.2s" fill="freeze" />
      </line>
      <line x1="-20" y1="20" x2="20" y2="-20" class="x">
        <animate attributeName="stroke-dasharray" from="0,56" to="56,0" dur="350ms" begin="0.6s" fill="freeze" />
      </line>
    </g>

    <!-- O at center -->
    <g transform="translate(100,100)">
      <circle r="28" class="o" stroke-dasharray="0,200">
        <animate attributeName="stroke-dasharray" from="0,176" to="176,0" dur="700ms" begin="1.1s" fill="freeze" />
      </circle>
    </g>

    <!-- X at top-right -->
    <g transform="translate(160,40)">
      <line x1="-20" y1="-20" x2="20" y2="20" class="x">
        <animate attributeName="stroke-dasharray" from="0,56" to="56,0" dur="350ms" begin="1.95s" fill="freeze" />
      </line>
      <line x1="-20" y1="20" x2="20" y2="-20" class="x">
        <animate attributeName="stroke-dasharray" from="0,56" to="56,0" dur="350ms" begin="2.35s" fill="freeze" />
      </line>
    </g>

    <!-- O at bottom-left -->
    <g transform="translate(40,160)">
      <circle r="28" class="o" stroke-dasharray="0,200">
        <animate attributeName="stroke-dasharray" from="0,176" to="176,0" dur="700ms" begin="2.9s" fill="freeze" />
      </circle>
    </g>

    <!-- X at mid-right -->
    <g transform="translate(160,100)">
      <line x1="-20" y1="-20" x2="20" y2="20" class="x">
        <animate attributeName="stroke-dasharray" from="0,56" to="56,0" dur="350ms" begin="3.9s" fill="freeze" />
      </line>
      <line x1="-20" y1="20" x2="20" y2="-20" class="x">
        <animate attributeName="stroke-dasharray" from="0,56" to="56,0" dur="350ms" begin="4.3s" fill="freeze" />
      </line>
    </g>

    <!-- small flourish: winning line animation (diagonal) -->
    <line x1="10" y1="10" x2="170" y2="170" stroke="#2ecc71" stroke-width="6" stroke-linecap="round" opacity="0">
      <animate attributeName="opacity" from="0" to="1" dur="400ms" begin="4.8s" fill="freeze" />
      <animate attributeName="stroke-dasharray" from="0,240" to="240,0" dur="600ms" begin="4.8s" fill="freeze" />
    </line>

    <!-- loop hint text -->
    <text x="90" y="195" font-size="12" text-anchor="middle" fill="#666">Tic-Tac-Toe — demo animation</text>
  </g>
</svg>
