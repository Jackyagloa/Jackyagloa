- 👋 Hi, I’m @Jackyagloa
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Jackyagloa/Jackyagloa is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

<code>
	// Cargamos el array de items en la variable $items
    $items = wp_get_nav_menu_items('principal');

    // Chequeamos que el array no está vacío
    if( !empty( $items ) ): ?>
        
        <nav class="mp__menu">
            
            <?php foreach ( $items as $item ): ?>
                
            <a class="mp__menu__i" href="<?php echo $item->url; ?>"><?php echo $item->post_title; ?></a>
                
            <?php endforeach; ?>
            
        </nav>
        
    <?php else: // Caso contrario mostramos un mensaje indicando que el menú no tiene elementos
    ?>
        
    <p class="msg msg--error">El menú no tiene enlaces cargados.</p>
        
    <?php endif; ?>
</code>
