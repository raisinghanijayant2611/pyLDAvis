.. :changelog:

History
-------

3.4.0 (2023-02-12)
~~~~~~~~~~~~~~~~~~

* Adding testing for Python 3.10, 3.11, move default version to Python 3.10.
* Tox testing: No module named 'sklearn.manifold'; 'sklearn' is not a package.
  * Rename sklearn.py to lda_model.py.
* ValueError: The parameter init="pca" cannot be used with metric="precomputed".
* Update sklearn.py #239.
* fixes error of get_feature_names removal #235.
* Remove "sklearn" from requirements #234
* Bump joblib from 1.0.1 to 1.2.0 dependencies #231.
* Fixing for small number of topics #229.
* Bump numpy from 1.20.1 to 1.22.0 dependenciesv #227.
* License correction #224.
* Fix background color in Notebooks with dark themes #222.
* Start building Wheels alongside sdist #221

3.3.1 (2021-03-24)
~~~~~~~~~~~~~~~~~~

* Restored x-axis scale labels for term bars #200.
* import pyLDAvis.gensim_models as gensimvis
* Deleted orphaned files.
* Update .gitignore for notebooks/* models, data.

3.3.0 (2021-03-16)
~~~~~~~~~~~~~~~~~~

* Python 3.7, 3.8, 3.9: dropped 2.7, 3.5, 3.6 support.
* RuntimeWarning: divide by zero encountered in log #174.
* Deprecation warning due to invalid escape sequences #166.
* `python setup.py test` is deprecated.
* FutureWarning: pandas.util.testing is deprecated.

3.2.2 (2021-02-19)
~~~~~~~~~~~~~~~~~~

* Fix browser caching of cdn.jsdelivr files.
* update ldavis.js to match ldavis.3.0.0.js

3.2.1 (2021-02-17)
~~~~~~~~~~~~~~~~~~

* Fix missing labels and other D3.V3 to D3.V5 issues.
* Revert the indexing changes i.e. (startIndex - 1).
* Removed some unused GLOBALs.

3.2.0 (2021-02-10)
~~~~~~~~~~~~~~~~~~

* Switches the CDN to cdn.jsdelivr to get accurate mime types.

3.1.0 (2021-02-07)
~~~~~~~~~~~~~~~~~~

* Replaces rawgit CDN since it has been sunset.

3.0.0 (2021-02-06)
~~~~~~~~~~~~~~~~~~

* Upgrades D3 code to use the d3.v5.

2.1.2 (2018-02-06)
~~~~~~~~~~~~~~~~~~

* Fix pandas deprecation warnings.

2.1.1 (2017-02-13)
~~~~~~~~~~~~~~~~~~

* Fix `gensim` module to work with a sparse corpus #82.

2.1.0 (2016-06-30)
~~~~~~~~~~~~~~~~~~

* Added missing dependency on `scipy`.
* Fixed term sorting that was incompatible with pandas 0.19.x.

2.0.0 (2016-06-30)
~~~~~~~~~~~~~~~~~~

* Removed dependency on `scikit-bio` by adding an internal PCoA implementation.
* Added helper functions for scikit-learn LDA model! See the new notebook for details.
* Extended gensim helper functions to work with HDP models.
* Added scikit-learn's Multi-dimensional scaling as another MDS option when scikit-learn is installed.

1.5.1 (2016-04-15)
~~~~~~~~~~~~~~~~~~

* Add sort_topics option to prepare function to allow disabling of topic re-ordering.


1.5.0 (2016-02-20)
~~~~~~~~~~~~~~~~~~

* Red Bar Width bug fix

 In some cases, the widths of the red topic-term bars did not decrease (as they should have) from term \#1 to
 term \#R under the relevance ranking with $\lambda = 1$. In other words, when $\lambda = 1$, there were topics
 in which a narrow red bar was displayed above a wider red bar, which should never happen. The issue had to do
 with the way topic-term bar widths are computed, and is discussed in detail in #32.


In the end, we implemented a quick fix in which we compute term frequencies implicitly, rather than using those
supplied in the createJSON() function. The upside is that the red bar widths are now explicitly controlled to
produce the correct visualization. The downside is that the blue bar widths do not necessarily match the
user-supplied term frequencies exactly -- in fact, the new version of LDAvis ignores the user-supplied term
frequencies entirely. In a few experiments, the differences are small, and decrease (as a proportion of the true
term frequencies) as the true term frequencies increase.



1.4.1 (2016-01-31)
~~~~~~~~~~~~~~~~~~

* Included requirements.txt in MANIFEST to (hopefully) fix bad release.

1.4.0 (2016-01-31)
~~~~~~~~~~~~~~~~~~

* Updated to newest version of skibio for PCoA mds.
* requirements.txt cleanup
* New 'tsne' option for prepare, see docs and notebook for more info.


1.3.5 (2015-12-18)
~~~~~~~~~~~~~~~~~~

* Add explicit version info for scikit-bio since the API has changed.


1.3.4 (2015-11-16)
~~~~~~~~~~~~~~~~~~

* Gensim Python typo fix in imports. :/

1.3.3 (2015-11-13)
~~~~~~~~~~~~~~~~~~

* Gensim Python 2.x fix for absolute imports.

1.3.2 (2015-11-09)
~~~~~~~~~~~~~~~~~~

* Gensim prepare 25% speed increase, thanks @mattilyra!
* Pandas deprecation warnings are now gone.
* Pandas v0.17 is now being used.

1.3.1 (2015-11-02)
~~~~~~~~~~~~~~~~~~

* Updates gensim and other logic to be python 3 compatible.

1.3.0 (2015-08-20)
~~~~~~~~~~~~~~~~~~

* Fixes gensim logic and makes it more robust.
* Faster graphlab processing.
* kargs for gensim and graphlab are passed down to underlying prepare function.
* Requires recent version of pandas to avoid problems with our use of the newer `DataFrame.to_dict` API.

1.2.0 (2015-06-13)
~~~~~~~~~~~~~~~~~~

* Updates gensim logic to be clearer and work with Python 3.x.

1.1.0 (2015-06-02)
~~~~~~~~~~~~~~~~~~

* Fixes bug with GraphLab function that was producing bogus visualizations.

1.0.0 (2015-05-29)
~~~~~~~~~~~~~~~~~~

* First release on PyPI. Faithful port of R version with IPython support and helper functions for GraphLab & gensim.
