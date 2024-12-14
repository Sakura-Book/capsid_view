<!DOCTYPE html>
<html lang="en">
    <head>
        <!-- Replace "latest" by the specific version you want to use, e.g. "4.0.0" -->
        <script src="https://cdn.jsdelivr.net/npm/molstar@latest/build/viewer/molstar.js"></script>
        <!-- Replace "latest" by the specific version you want to use, e.g. "4.0.0" -->
        <link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/npm/molstar@latest/build/viewer/molstar.css" />
    </head>

    <body>
        <div id="viewer2" style="position: relative; width: 500px; height: 500px;"></div>
        <button class="button" onclick="loadView1();">View 1</button>
        <button class="button" onclick="loadView2();">View 2</button>
        <script>
            let theViewer;
            function load(viewer, url, replace) {
                fetch(url)
                    .then(response => response.text())
                    .then(text => molstar.PluginExtensions.mvs.MVSData.fromMVSJ(text))
                    .then(mvsData => molstar.PluginExtensions.mvs.loadMVS(viewer.plugin, mvsData, { sourceUrl: url, sanityChecks: true, replaceExisting: replace }));
            }
            function loadView1() {
                load(theViewer, 'https://raw.githubusercontent.com/molstar/molstar/master/examples/mvs/1cbs.mvsj', true);
            }
            function loadView2() {
                load(theViewer, 'https://raw.githubusercontent.com/molstar/molstar/master/examples/mvs/1cbs-focus.mvsj', true);
            }
            molstar.Viewer
                .create('viewer2', { layoutIsExpanded: false, layoutShowControls: false })
                .then(viewer => {
                    theViewer = viewer;
                    loadView1();
                });
        </script>
    </body>
</html>