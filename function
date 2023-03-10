<?php


add_filter( 'bricks/theme_styles/controls', 'element_theme_column_gap', 10, 1);

function element_theme_column_gap($theme_styles_controls) {

	$theme_styles_controls['container']['_columnGap'] = [
		'label'    => esc_html__( 'Column gap', 'bricks' ),
		'type'     => 'number',
		'units'    => true,
		'css'      => [
			[
				'property' => 'column-gap',
				'selector' => '.brxe-container',
			],
			[
				'property' => '--column-gap',
				'selector' => '.brxe-container > *',
			],
		],
		'required' => [ '_display', '=', [ '', 'flex' ] ],
	];

    return $theme_styles_controls;
};



add_filter( 'bricks/elements/container/controls', 'element_container_column_gap', 10, 1);

function element_container_column_gap($controls) {

	$controls['_columnGap'] = [
		'label'    => esc_html__( 'Column gap', 'bricks' ),
		'type'     => 'number',
		'units'    => true,
		'css'      => [
			[
				'property' => 'column-gap',
			],
			[
				'selector'	=> '> *',
				'property' => '--column-gap',
			],
		],
		'required' => [ '_display', '=', 'flex' ],
	];

    return $controls;
};


add_filter( 'bricks/elements/block/controls', 'element_block_column_span', 10, 1);

function element_block_column_span($controls) {

	$controls_top['_columnSpan'] = [
		'tab'       => 'content',
		'label'     => esc_html__( 'Column span', 'bricks' ),
		'type' 		=> 'number',
		'min'		=> 1,
		'max'		=> 12,
		'step'		=> 1,
		'inline' => true,
		'css'         => [
			[
				'property'	=> '--column-span',
				'value'		=> '%s',
			],
			[
				'property' 	=> 'max-width',
				'value'		=> 'calc((100% - 11 * var(--column-gap, 0px)) * var(--column-span) / 12 + (var(--column-span) - 1) * var(--column-gap, 0px))'
			],
		]
	];

	return array_merge($controls_top, $controls);

};
