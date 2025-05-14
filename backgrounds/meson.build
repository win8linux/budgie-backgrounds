backgrounds = [
    'abstract-spiral.jxl',
    'beacon-street-sunset.jxl',
    'blue-periwinkle.jxl',
    'canyon-wren.jxl',
    'casa-mila.jxl',
    'extreme-desert-hike.jxl',
    'high-trestle-trail.jxl',
    'lake-sherburne.jxl',
    'oakland-zoo-otters.jxl',
    'ocean-waves.jxl',
    'perched-osprey.jxl',
    'piazza-gae-aulenti.jxl',
    'roman-colosseum.jxl',
    'saturnian-profile.jxl',
    'singaporean-cityscape.jxl',
    'tea-gardens.jxl',
    'valley-midnight.jxl',
    'waves-midnight.jxl',
    'the-spices-of-life.jxl',
]

backgrounds_dir = join_paths(path_datadir, 'backgrounds', 'budgie')

mogrify = find_program('mogrify')
jhead = find_program('jhead')

script = find_program(join_paths(meson.source_root(), 'scripts', 'optimizeImage.sh'))

optimized_background_targets = []
foreach background : backgrounds
    optimized_background_targets += custom_target(background,
        input: background,
        output: '@BASENAME@.jxl',
        command: [script, '@INPUT@', '@OUTPUT@'],
        install: true,
        install_dir: backgrounds_dir
    )
endforeach
