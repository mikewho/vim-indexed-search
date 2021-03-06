# IndexedSearch.vim by [Yakov Lerner](http://www.vim.org/account/profile.php?user_id=2342)

This is a minor fork of the original, modified to center matches in the window 
and open folds if necessary. <bobroski@gmail.com>

[See the plugin page at vim.org.](http://www.vim.org/scripts/script.php?script_id=1682)

---

    This plugin redefines 6 search commands (/,?,n,N,*,#). At every 
    search command, it automatically prints 
           "At match #N out of M matches". 
    -- the total number of matches (M) and the number(index) of current 
    match (N). This helps to get oriented when searching forward and 
    backward. 
    
    To try out the plugin, source it and play with N,n,*,#,/,? commands. 
    There are no new commands and no new behavior to learn. 
    Just watch the bottom line when you do /,?,n,N,*,#. 
    
    Works on vim6 and vim7.  Won't cause slowdown 
    on very large files (but then counters are not displayed). 
    
    ----------------------------------------------------- 
    Checking At which Match Number You Are 
    ..................................................... 
    You can press g/ or \\ or \/ (that's backslach then slash),to show 
    at which match index you are, without moving the cursor. 
    Messages are: 
        At Nth match of M (if cursor is exactly on the match) 
        Betwen matches N1-N2 of M (if cursor is between matches) 
        At single match 
        Before first match, of N 
        After last match, of N 
    Command  ':ShowSearchIndex'  shows same information. 
    ------------------------------------------------------ 
    To disable colors for messages, set 'let g:indexed_search_colors=0'. 
    ------------------------------------------------------ 
    Performance.     Plugin bypasses the calculation of match index when 
    it would take too much time (too many matches, too large file). You can 
    tune performance limits, look into script sources after comment 
    "Performance tuning limits". 
    ------------------------------------------------------ 
    In case of bugs and wishes, please email to:   
    iler.ml at gmail.com 
    ------------------------------------------------------ 
    To show slightly shorter messages, define 'let g:indexed_search_shortmess=1' 
     
    install details
    Short instructions: drop script into your personal plugin directory (~/.vim/plugin). 

    Detailed instructions: 
    1. Download script IndexedSearch.vim from the link below. 
    2. Create directory ~/.vim/plugin if it does not exist: 
                     mkdir -p ~/.vim/plugin 
       (your personal plugin directory). 
    3. Copy script IndexedSearch.vim into ~/.vim/plugin directory. 
    4. Restart vim 
