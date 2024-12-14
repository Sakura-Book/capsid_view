<!DOCTYPE html>
<html lang="en">
    <head>
        <!-- Replace "latest" by the specific version you want to use, e.g. "4.0.0" -->
        <script src="https://cdn.jsdelivr.net/npm/molstar@latest/build/viewer/molstar.js"></script>
        <!-- Replace "latest" by the specific version you want to use, e.g. "4.0.0" -->
        <link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/npm/molstar@latest/build/viewer/molstar.css" />
    </head>

    <body>
        <div id="viewer3" style="position: relative; width: 500px; height: 500px;"></div>
        <script>
            // Build an ad-hoc MVS view
            const builder = molstar.PluginExtensions.mvs.MVSData.createBuilder();
            const structure = builder
                .download({ url: 'https://www.ebi.ac.uk/pdbe/entry-files/1cbs.bcif' })
                .parse({ format: 'bcif' })
                .modelStructure({});
            structure
                .component({ selector: 'polymer' })
                .representation({ type: 'cartoon' })
                .color({ color: 'green' });
            structure
                .component({ selector: 'ligand' })
                .label({ text: 'Retinoic acid' })
                .focus({})
                .representation({ type: 'ball_and_stick' })
                .color({ color: '#cc3399' });
            const mvsData = builder.getState();
            // Initialize viewer and load MVSJ
            molstar.Viewer
                .create('viewer3', { layoutIsExpanded: false, layoutShowControls: false })
                .then(viewer => molstar.PluginExtensions.mvs.loadMVS(viewer.plugin, mvsData, { sourceUrl: undefined, sanityChecks: true, replaceExisting: false }));
        </script>
    </body>
</html>