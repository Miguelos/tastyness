import sublime
import sublime_plugin
import shutil
import filecmp


class SwitchCommand(sublime_plugin.ApplicationCommand):
    def run(self):
        folder = '/home/vic/.config/sublime-text-2/Packages/User/'
        latex_src = folder + 'LaTeX.sublime-build.latex'
        xetex_src = folder + 'LaTeX.sublime-build.xetex'
        dest = folder + 'LaTeX.sublime-build'
        if filecmp.cmp(dest, latex_src):
            sublime.status_message("Switching to XeTeX")
            shutil.copy(xetex_src, dest)
        elif filecmp.cmp(dest, xetex_src):
            sublime.status_message("Switching to LaTeX")
            shutil.copy(latex_src, dest)
