class Solution {
    public int expressiveWords(String S, String[] words) {
        int count = 0;
        for(int i = 0; i < words.length; i ++){
            if(check(S, words[i])){
                count ++;
            }
        }
        return count;
    }
    public boolean check(String S, String str){
        int s = 0;
        int l = 0;
        while(l < str.length() && s < S.length()){
            if(S.charAt(s) != str.charAt(l)){
                return false;
            }
            char temp = S.charAt(s);
            if(getAppearance(S, s) < getAppearance(str, l)){
                return false;
            }
            if(getAppearance(S, s) < 3){
                s ++;
                l ++;
            }else{
                
                while(s < S.length() && S.charAt(s) == temp){
                    s ++;
                }
                 while(l < str.length() && str.charAt(l) == temp){
                    l ++;
                }
            }
        }
        if(l == str.length() && s == S.length()){
             return true;
        }else{
            return false;
        }
       
    }
    public int getAppearance(String str, int index){
        int cnt = 1;
        while(index < str.length() - 1 && str.charAt(index) == str.charAt(index + 1)){
            index ++;
            cnt ++;
        }
        return cnt;
    }
}
