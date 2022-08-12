---
title: Downloading OpenSlide
permalink: /download/
redirect_from:
  - /Download/
---

{% include links.md %}

OpenSlide and its official language bindings are available under the terms
of the [GNU Lesser General Public License, version 2.1][license].

## Source

#### OpenSlide (stable API)
{% assign package = 'openslide' %}
{% assign releases = site.data.releases.c %}
{% include source-release-table.md %}

#### OpenSlide Python interface (stable API)
{% assign package = 'openslide-python' %}
{% assign releases = site.data.releases.python %}
{% include source-release-table.md %}

#### OpenSlide Java interface (still unstable API, subject to change)
{% assign package = 'openslide-java' %}
{% assign releases = site.data.releases.java %}
{% include source-release-table.md %}


## Windows Binaries

Problems with these binaries can be reported [here][winbuild-issues].
If you're looking for the bleeding edge,
[nightly development builds][snapshots-windows] are also available.

<div class="releases">
  <table>
    {% for release in site.data.releases.winbuild %}
      <tr class="{% cycle 'winbuild': 'odd', 'even' %}">
        <th>{{ release.date }}</th>
        <td><a href="https://github.com/openslide/openslide-winbuild/releases/download/v{{ release.date|remove:'-' }}/openslide-win32-{{ release.date|remove:'-' }}.zip">32-bit</a></td>
        <td><a href="https://github.com/openslide/openslide-winbuild/releases/download/v{{ release.date|remove:'-' }}/openslide-win64-{{ release.date|remove:'-' }}.zip">64-bit</a></td>
        <td><a href="https://github.com/openslide/openslide-winbuild/releases/download/v{{ release.date|remove:'-' }}/openslide-winbuild-{{ release.date|remove:'-' }}.zip">Corresponding sources</a></td>
      </tr>
    {% endfor %}
  </table>
</div>


## Distribution Packages

<table class="pinfo">
  <thead>
    <tr>
      <th>Platform</th>
      <th>Distribution</th>
      <th>OpenSlide</th>
      <th>OpenSlide Python</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Linux</th>
      <th><a href="https://fedoraproject.org/">Fedora</a></th>
      <td><code>dnf install openslide</code></td>
      <td><code>dnf install python3-openslide</code></td>
    </tr>
    <tr>
      <th>Linux</th>
      <th>
        <a href="https://www.debian.org/">Debian</a><br>
        <a href="https://ubuntu.com/">Ubuntu</a>
      </th>
      <td><code>apt-get install openslide-tools</code></td>
      <td>
        <code>apt-get install python3-openslide</code><br>
      </td>
    </tr>
    <tr>
      <th>Linux</th>
      <th><a href="https://www.opensuse.org/">openSUSE</a></th>
      <td><code>zypper install openslide-tools</code></td>
      <td></td>
    </tr>
    <tr>
      <th>Linux</th>
      <th>
        <a href="https://www.redhat.com/products/enterprise-linux/">Red Hat Enterprise Linux</a><br>
        <a href="https://www.centos.org/">CentOS</a><br>
        <a href="https://www.scientificlinux.org/">Scientific Linux</a>
      </th>
      <td>
        <i>First, install <a href="https://fedoraproject.org/wiki/EPEL">EPEL</a>.</i><br>
        <code>yum install openslide</code><br>
        <i>(RHEL/CentOS/Scientific Linux &ge; 7)</i>
      </td>
      <td>
        <i>First, install <a href="https://fedoraproject.org/wiki/EPEL">EPEL</a>.</i><br>
        <code>yum install python3-openslide</code><br>
        <i>(RHEL/CentOS Stream &ge; 8)</i>
      </td>
    </tr>
    <tr>
      <th>Mac OS X</th>
      <th><a href="https://www.macports.org/">MacPorts</a></th>
      <td><code>port install openslide</code></td>
      <td><code>port install py310-openslide</code></td>
    </tr>
    <tr>
      <th>Mac OS X</th>
      <th><a href="https://brew.sh/">Homebrew</a></th>
      <td><code>brew install openslide</code></td>
      <td></td>
    </tr>
    <tr>
      <th>Python</th>
      <th><a href="https://pypi.org/">PyPI</a></th>
      <td></td>
      <td><code>python3 -m pip install openslide-python</code></td>
    </tr>
    <tr>
      <th>Python</th>
      <th><a href="https://anaconda.org/conda-forge">Anaconda</a></th>
      <td></td>
      <td><code>conda install -c conda-forge openslide</code></td>
    </tr>
  </tbody>
</table>


## Version Control

[Git][git] repositories are available:

<table class="pinfo">
  <thead>
    <tr>
      <th>Repository</th>
      <th>Clone command</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th><a href="https://github.com/openslide/openslide">OpenSlide</a></th>
      <td><code>git clone https://github.com/openslide/openslide.git</code></td>
    </tr>
    <tr>
      <th><a href="https://github.com/openslide/openslide-python">OpenSlide Python</a></th>
      <td><code>git clone https://github.com/openslide/openslide-python.git</code></td>
    </tr>
    <tr>
      <th><a href="https://github.com/openslide/openslide-java">OpenSlide Java</a></th>
      <td><code>git clone https://github.com/openslide/openslide-java.git</code></td>
    </tr>
    <tr>
      <th><a href="https://github.com/openslide/openslide-winbuild">Windows build scripts</a></th>
      <td><code>git clone https://github.com/openslide/openslide-winbuild.git</code></td>
    </tr>
    <tr>
      <th><a href="https://github.com/openslide/builds">Nightly build infrastructure</a></th>
      <td><code>git clone https://github.com/openslide/builds.git</code></td>
    </tr>
    <tr>
      <th><a href="https://github.com/openslide/openslide.github.io">Website</a></th>
      <td><code>git clone https://github.com/openslide/openslide.github.io.git</code></td>
    </tr>
  </tbody>
</table>

<!-- Ensure spacing above footer -->
<span></span>

[git]: https://git-scm.com/
