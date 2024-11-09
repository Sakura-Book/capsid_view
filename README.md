# capsid_view

<!DOCTYPE html>
<html lang="en">
    <head>
        <!-- Replace "latest" by the specific version you want to use, e.g. "4.0.0" -->
        <script src="https://cdn.jsdelivr.net/npm/molstar@latest/build/viewer/molstar.js"></script>
        <!-- Replace "latest" by the specific version you want to use, e.g. "4.0.0" -->
        <link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/npm/molstar@latest/build/viewer/molstar.css" />
    </head>

    <body>
        <div id="viewer1" style="position: relative; width: 500px; height: 500px;"></div>
        <script>
            const sourceUrl = 'https://raw.githubusercontent.com/Sakura-Book/molstar_test/main/mvsj_files/T_1/Circoviridae/Circovirus/6dzu.mvsj';
            molstar.Viewer
                .create('viewer1', { layoutIsExpanded: false, layoutShowControls: false })
                .then(viewer => viewer.loadMvsFromUrl(sourceUrl, 'mvsj'));
        </script>
    </body>
</html>